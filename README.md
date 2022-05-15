[![.github/workflows/gh-pages.yml](https://github.com/RICORA/alg-wiki/actions/workflows/gh-pages.yml/badge.svg)](https://github.com/RICORA/alg-wiki/actions/workflows/gh-pages.yml)


# はじめに

このwikiは[RICORA言語班](https://alg.tus-ricora.com)での知見を集積するためのものです。

## 内容

いまあるもの
- [Git / GitHubのつかいかた](git-tutorial.html)
- [Markdownのつかいかた](md-tutorial/md1.html)
- [VSCodeのつかいかた](vscode-tutorial/md1.html)

書かれるであろうもの
- [hugoのつかいかた / alg-HPにPRを出してみよう]()
- [Marpのつかいかた]()
- [Pandocのつかいかた]()
- [Gnuplotのつかいかた]()


### 環境構築する

このページはHonkitを使っています。

くわしくは[honkitのドキュメント](https://honkit.netlify.app/)を読んで編集してください。

インストールする際の手順:

  0. npmとnodeとnpxを入れておく。わからなければ[node.jsの環境構築をする]()を参照してください。
  
  1. 以下のコマンドを打つ
  ```
    npm init --yes
    npm install honkit --save-dev
  ```

  2. ディレクトリに移動し、`npm run serve`を打って出てきたURLにアクセス
  ```
    cd alg-wiki && npm run serve
  ```

困ったときは[JS Primer](https://jsprimer.net/)がHonKitで書かれているのでそちらのGHとかを見るといいはず。

なにか問題があればtwitter[@NAUS3E](https://twitter.com/NAUS3E)に連絡、またはissueを立ててください。
