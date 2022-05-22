# SSH の使い方
## SSH とは

`Secure Shell` の略で、ネットワーク上にある端末（サーバ、ルータなど）に安全に操作するためのプロトコルである。
接続手段は パスワード方式と公開鍵認証の 2 パターン用意されている。

この記事では [GitHub](https://github.com) との通信を行うことを想定しているため、後者の公開鍵認証を取り上げる。

### 公開鍵認証とは
1 つの鍵（共通鍵）だけでやり取りを行うと、その鍵が外部に流出してしまったときに、自分と通信相手以外の第三者までが、解読できてしまう。
それを解決するために誕生したのが公開鍵認証である。

公開鍵を用いて、 `Bob`  が  `Alice`  に暗号文を送る手順としては、
1.  `Bob` が公開鍵と秘密鍵の異なる 2 つの鍵を用意する。（ 2 つの鍵は対応している）
2.  `Bob` は  `Alice` に公開鍵を提示する。（公開鍵では暗号文を復号できないので、Twitter みたいな不特定多数の見れるところにのせても大丈夫）
3.  `Alice` は `Bob` の提示した公開鍵を使って送りたい文章を暗号化し、`Bob` に送る。
4.  `Bob` は `Alice` から送られてきた暗号文を秘密鍵を用いて復号する。 

のようになる。実際メールなどを暗号化する際には GPG というものを使うのが一般的である。

## GitHub で SSH 接続をする方法
今回は RSA よりも鍵長が短く高速に処理ができる エドワーズ曲線デジタル署名アルゴリズムの `ED25519` を用いる。

### 公開鍵と秘密鍵を生成する
1. Windows の場合は Git Bash を、Mac, GNU/Linux の場合は ターミナルを開く。
2. 下記のコマンドをコマンドラインに入力する。

 ```
$ ssh-keygen -t ed25519
```
そうすると
```
Generating public/private ed25519 key pair.
Enter file in which to save the key (/Users/user/.ssh/id_ed25519):
```
どこに保存するか聞かれるので、特に指定ながければ `Enter` を押す。
次に、
```
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```
と新しいパスワードを入力するよう求められるので、適切なパスワードを設定し、 `Enter` を押し、先程設定したパスワードを入力し`Enter`を押す。
そうするとホームディレクトリの直下に `.ssh` ができ、その中に `id_ed25519` と `id_ed25519.pub` の2つの鍵が生成されます。

### GitHub に公開鍵をプッシュする
https://github.com/settings/ssh 

ここで 先程作った 公開鍵を登録する。

1. New SSH key をクリックする。

![ssh-add-ssh-key](photo/ssh-add-ssh-key.png)

2. 適当な Title を設定し、

Macの場合は `$ pbcopy < ~/.ssh/id_ed25519.pub`

Windows の場合は `$ clip < ~/.ssh/id_ed25519.pub`

で公開鍵をコピーし `Key` の入力フォームにペーストする。

![ssh-key-paste](photo/ssh-key-paste.png)

3.  `$ ssh -T git@github.com` とコマンドラインに入力し、パスワードを入力して、接続できてるか確認する。

```
Hi "GitHub のユーザー名"! You've successfully authenticated, but GitHub does not provide shell access.
```

と出てきたら成功！