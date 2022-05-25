# プログラムを書く環境を整える

この記事にしたがってインストールなどをしていくことで、サークルの活動にプログラムを書けば参加できる環境構築ができるはずです。それでは、始めていきましょう。

## プログラムを最低限書けるようにしよう

### VS Codeを入れる
##### Windows

   1. [このページ](https://www.javadrive.jp/vscode/install/index1.html)を読んでインストールする
   2. ショートカットから起動できることを確認

##### Mac

   1. 先にこのページの下にある`homebrew`を入れる
   2. `brew install --cask visual-studio-code`を入力
   3. `code`と打って起動できることを確認

- (Mac) Xcode Command Line Tools (CLT)を入れる

--- 

## パッケージマネージャーでソフトを管理しよう


### Windows


##### Chocolateyを入れよう
   1. [このページ](https://chocolatey.org/install#individual)に書いてあることに従う。
   - Powershellを管理者権限で起動して、サイトにある文言に従う。
   - 管理者権限を持っていない場合、[このページ](https://docs.chocolatey.org/en-us/choco/setup#non-administrative-install)に従おう。
   - `choco -h`でヘルプ画面が見えたらOK

- Mac

   - homebrewを入れよう
  

### Linux

   割愛。`apt`なり`pacman`を使っているはずなので自分で調べてね

--- 

## gitが使えるようにしよう

### Windows

1. Powershellを起動し、`choco install git -y`を打つ
2. `git -h`でヘルプ画面が出ることを確認できればOK

- Mac

   - brewでgitを入れよう

### Linux

   - マネージャ(`apt`とか`pacman`)で入れる。問題が生じたらArch wikiかdebianのメーリスとか見る。

--- 

## hugoをインストールしよう

[hugoのgetting started](https://gohugo.io/getting-started/installing/)に従おう。以下では簡単に記しておく。サークルのページで使っているのは**Hugo-extended**なので、インストール時は気をつけよう。

##### Windows
   1. `Chocolatey`を導入している環境なら`choco install hugo-extended -confirm`をPowershellなどに入力
   2. `hugo -h`とかでヘルプ画面が出ればOK

##### Mac
   1. homebrewを使っているなら `brew install hugo`
      - tarballがいいならtarballを拾ってきて`tar xvf`とかする
   2. `hugo -h`とかでヘルプ画面が出ればOK

##### Linux
   - `apt`でとってこれるバージョンが古いことが多い（debianのパッケージのリリースサイクルを考えたら当たり前）なので、[ここ](https://github.com/gohugoio/hugo/releases)にあるバイナリを`/usr/local/bin`とか`/usr/bin/`とか`$HOME/.bin/`とかに配置する。debianとかなら`dpkg`でもよい
   

### インストールが終わったら

サークルのHPを手元で動かしてみよう。手順は以下の通り

1. `git clone --recursive (repo URL)`
2. `cd alg-HP`
3. `hugo server`

これで`http://localhost:1313`にアクセスして、[ここ](alg.tus-ricora.com)にあるようなサイトが表示されていれば成功！

--- 

## node.jsをインストールしよう

要追記。

- Windows

- Mac

- Linux
