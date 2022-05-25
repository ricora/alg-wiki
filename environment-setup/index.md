# プログラムを書く環境を整える

この記事にしたがってインストールなどをしていくことで、サークルの活動にプログラムを書けば参加できる環境構築ができるはずです。それでは、始めていきましょう。

## A. プログラムを最低限書けるようにしよう

#### (macOSのみ) Xcode Command Line Tools (CLT)を入れる

1. Spotlightなどを使ってターミナル.appを起動しよう。このあとも使い続けるのでdockに入れてもいいかも
2. ターミナルで`xcode-select --install`と打つ。結構時間がかかるので、じっくり待とう。
3. エラー表示が出てなければ導入完了！

### VS Codeをインストールする
#### Windows

1. [このページ](https://www.javadrive.jp/vscode/install/index1.html)を読んでインストールする
2. ショートカットから起動できることを確認しよう

#### Mac

1. 先にこの下のパッケージマネージャーの節にある`homebrew`を入れる
2. `brew install --cask visual-studio-code`を入力
3. SpotlightでVS Codeを見つけて起動できればとりあえずOK
4. VS Codeを起動し、Command + Shift + Pを押してから、`shell command`と入力。PATHに`code`をインストールを選択
5. ターミナルでcodeと入力し、VS Codeが立ち上がることを確認

--- 

## B. パッケージマネージャーでソフトを管理しよう


#### Windows - Chocolateyを導入しよう

1. [このページ](https://chocolatey.org/install#individual)にアクセス
2. Powershellを管理者権限で起動する。サイトの`Install Chocolatey for Individual Use`の真ん中にあるコマンドを入力し、エンターキーを押す。
3. 管理者権限を持っていない場合、[このページ](https://docs.chocolatey.org/en-us/choco/setup#non-administrative-install)に従おう。
4. `choco -?`でヘルプ画面が見えたらOK

#### Mac - homebrewを導入しよう
  
1. [brew.sh](https://brew.sh/)の`Install Homebrew`の下にあるスクリプトをコピーして、ターミナルに貼り付けて、エンターを押す
2. `brew --version`でバージョンが表示されたらOK

#### Linux
割愛。`apt`なり`pacman`を使っているはずなので自分で調べてね

##### なぜパッケージマネージャーが必要なのか

パッケージマネージャーの強みは、コマンド一つでソフトウェアをインストールして、使用可能な状態にもっていけることです。パッケージマネージャーがなければ、すべてのソフトウェアの依存関係をすべて調べて、必要そうなライブラリをかき集め、やっとソフトウェアが動くということになります。ストレスフルですね。パッケージマネージャーは、インストールだけでなく、削除や更新、ソフトウェアの検索もできるので、導入をおすすめしています。

--- 

## C. gitをインストールしよう

#### Windows

1. Powershellを起動し、`choco install git -y`を打つ
2. `git -h`でヘルプ画面が出ることを確認できればOK

#### macOS

もともと`xcode-select`に入っているので、`git -h`でヘルプ画面を確認できればOK。

違うバージョンの`git`を使いたい人は`brew install git`で

#### Linux

マネージャ(`apt`とか`pacman`)で入れる。問題が生じたらArch wikiかdebianのメーリスとか見る。できれば一次ソースを見るようにしたほうがいい。

--- 

## D. Pythonをインストールしよう

Pythonが使えると便利なことが多いので紹介しておく。

#### Windows

詳しくは[このページ](https://www.python.jp/install/windows/install.html)にあるよ。

1. [ダウンロードリンク](https://pythonlinks.python.jp/en/index.html)から好きなバージョンのファイルをダウンロード。
2. ダウンロードしたファイルを実行し、インストールウィザードに従う。一番最初に`Add Python 3.x to PATH`をクリックし、チェックマークがついていることを確認。
3. 終わったら、コマンドプロンプトで`python --version`を打って、バージョンが出ればOK

#### macOS

1. `brew install python3`をターミナルで打つ。
2. `python3 --version`と打ってバージョンが出ればOK

#### Linux

略。ちなみに`gnome`は`apt remove python3`で破壊できる。

---

## E. hugoをインストールしよう

[hugoのgetting started](https://gohugo.io/getting-started/installing/)に従おう。以下では手順を簡単に記しておく。サークルのページで使っているのは**Hugo-extended**なので、インストール時にhugo-extendedをインストールするようにしよう。

#### Windows
   1. `Chocolatey`を導入している環境なら`choco install hugo-extended -confirm`をPowershellなどに入力
   2. `hugo -h`とかでヘルプ画面が出ればOK

#### Mac
   1. homebrewを使っているなら `brew install hugo`
      - tarballがいいならtarballを拾ってきて`tar xvf`とかする
   2. `hugo -h`とかでヘルプ画面が出ればOK

#### Linux
   - `apt`でとってこれるバージョンが古いことが多い（debianのパッケージのリリースサイクルを考えたら当たり前）なので、[ここ](https://github.com/gohugoio/hugo/releases)にあるバイナリを`/usr/local/bin`とか`/usr/bin/`とか`$HOME/.bin/`とかに配置する。debianとかなら`dpkg`でもよい
   

### インストールが終わったら

サークルのHPを手元で動かしてみよう。打つコマンドは以下の通り。

1. `git clone --recursive https://github.com/RICORA/alg-HP.git`
2. `cd alg-HP`
3. `hugo server`

3.まで終わったら`http://localhost:1313`にアクセスして、[ここ](https://alg.tus-ricora.com)にあるようなサイトが表示されていれば成功！

--- 

## F. node.jsをインストールしよう

#### Windows

1. [node.jsのダウンロードページ](https://nodejs.org/ja/download/)からWindows Installerを選んで、.pkgファイルをダウンロード
2. ダウンロードしたインストーラーを開いて、ウィザードの指示に従ってインストールする
3. Powershellかコマンドプロンプトを開いて、`node --help`と`npm help`の両方でヘルプ画面が出ればOK

#### Mac

1. [node.jsのダウンロードページ](https://nodejs.org/ja/download/)からmacOS Installerを選んで、.pkgファイルをダウンロード
2. ウィザードが開くので、ウィザードの指示にしたがってインストールする
3. ターミナルを開いて`node --help`と`npm help`の両方でヘルプ画面が出ればOK

#### Linux

1. `nvm`を入れる。[ここ](https://github.com/nvm-sh/nvm#installing-and-updating)にあるコマンドをコピペ。
2. `nvm install (version)`とか`nvm install latest`で`node.js`を入れる
3. `node --help`と`npm help`でヘルプ画面が出ればOK

### インストールが終わったら

サークルのwikiを手元で動かしてみよう！打つコマンドは以下の通り。

1. `git clone https://github.com/RICORA/alg-wiki.git`
2. `cd alg-wiki`
3. `npm i honkit katex`
4. `npm run serve`

4.まで終わったら`http://localhost:4000`にアクセスして、[ここ](https://alg-wiki.tus-ricora.com)にあるようなサイトが表示されていれば成功！

