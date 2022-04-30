# Markdown の使い方について
この記事は [日本語 markdown の会](http://www.markdown.jp/syntax/), [Qiita 株式会社](https://qiita.com/Qiita/items/c686397e4a0f4f11683d) , [Titech traP ](https://trap.jp/post/371/)  を参考にした．より詳しいことが知りたいならばこちらを参考にしてほしい．
## Markdown って？美味しいの？
### Markdown の概要
Markdown は[マークアップ言語](https://ja.wikipedia.org/wiki/%E8%BB%BD%E9%87%8F%E3%83%9E%E3%83%BC%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97%E8%A8%80%E8%AA%9E)の 1 つであり，変換ツールを噛ますことにより，HTML や $\LaTeX$ などの別のマークアップ言語に変換をすることができる．

また，Pandoc や Marp, SATySFi などを用いれば高品質な PDF を生成することも可能である．すなわち，ツール次第であらゆることが可能である．

最近の技術系プラットフォームでは Markdown 記法をサポートしているものが多い．（GitHub, Discord, Qiita など）そのため，Markdown はプログラミングを学ぶ上では知っておいて損はない．

### Markdownのメリット
- HTML などと比べ，とても簡潔に書くことができる．
-  覚えやすい記述方式である．
- 数式や表などを入力できる．

などが挙げられる．

# Markdown の記述方法
## 見出し
# h1
```
# h1
```
## h2
```
## h2
```
### h3
```
### h3
```
## 段落
空の行で間を開ければ良い．

東京理科大学

理工学部

```
東京理科大学
[空]
理工学部
```
## 区切り線
---
あああ
___
あああ
***
あああ

```
---
あああ
___
あああ
***
あああ
```

## 箇条書き
半角ハイフン ( - )  + スペース
- RICORA
```
- RICORA
```
## 引用
半角大なり ( > ) を記述する．途中で ( > ) を増やすことにより 2 段引用が可能だ．
> Markdown（マークダウン）は、文書を記述するための軽量マークアップ言語のひとつである。本来はプレーンテキスト形式で手軽に書いた文書からHTMLを生成するために開発されたものである。
>  > Wikipediaより
```
> Markdown（マークダウン）は、文書を記述するための軽量マークアップ言語のひとつである。本来はプレーンテキスト形式で手軽に書いた文書からHTMLを生成するために開発されたものである。
>  > Wikipediaより
```
##  画像
```
![説明](URL)
```
![RICORA](https://avatars.githubusercontent.com/u/33452053)
```
![RICORA](https://avatars.githubusercontent.com/u/33452053)
```

## 数式
```$$``` で囲った間に $\TeX$ 記述をすれば表示される．

$\left(\bigcap_{i=1}^\infty\bigcup_{j=i}^\infty A_j\right)=0$
```
$\left(\bigcap_{i=1}^\infty\bigcup_{j=i}^\infty A_j\right)=0$
```
## 表
|普通|中央揃え|右揃え|
| - | :-: | -: |
|あ|い|う|
```
|普通|中央揃え|右揃え|
| - | :-: | -: |
|あ|い|う|
```

## ソースコード
``` ``` ```で挟む（記入例ではやむなく \ を入れているが，必要ない．）
```C++
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

```
\```C++
#include <iostream>
int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
\```
```

## リンク
[RICORA アルゴリズム班](https://alg.tus-ricora.com/)
```
[RICORA アルゴリズム班](https://alg.tus-ricora.com/)
```
