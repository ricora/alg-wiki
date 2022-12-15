# alg-wiki

[![.github/workflows/gh-pages.yml](https://github.com/RICORA/alg-wiki/actions/workflows/gh-pages.yml/badge.svg)](https://github.com/RICORA/alg-wiki/actions/workflows/gh-pages.yml)


## Overview

このWikiは[RICORA Programming Team](https://alg.tus-ricora.com)での知見を集積するためのものです。

## Contribution

ページの生成には[Honkit](https://github.com/honkit/honkit)を使っています。詳しくは[Honkitのドキュメント](https://honkit.netlify.app/)を読んで編集してください。

なにか問題や疑問点があれば[Issues](https://github.com/RICORA/alg-wiki/issues)に投げてください。

困ったときはHonkitが使われている他のドキュメントのリポジトリ(例えば[JavaScript Primer](https://jsprimer.net/)など)が参考になりそうです。

### Requirement

[Node.js](https://nodejs.org/)が必要です。わからなければ[Node.jsの環境構築をする](environment-setup/#f-nodejsをインストールしよう) を参照してください。

### Installation

`README.md`や`package.json`などがあるディレクトリに移動し、以下のコマンドを実行してください。

```
npm install
```

### Preview

以下のコマンドを実行すると[http://localhost:4000](http://localhost:4000)でプレビューができます。

```
npm run serve
```
