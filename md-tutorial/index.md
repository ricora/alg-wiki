# Markdown の使い方について
この記事は [日本語 markdown の会](http://www.markdown.jp/syntax/)、[Qiita 株式会社](https://qiita.com/Qiita/items/c686397e4a0f4f11683d)、[Titech traP ](https://trap.jp/post/371/)  を参考にした。より詳しいことが知りたいならばリンク先を参考にしてほしい。
## Markdown って？美味しいの？
### Markdown の概要

Markdown は[マークアップ言語](https://ja.wikipedia.org/wiki/%E8%BB%BD%E9%87%8F%E3%83%9E%E3%83%BC%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97%E8%A8%80%E8%AA%9E)の 1 つであり、変換ツールを噛ますことにより、HTML や $\LaTeX$ などの別のマークアップ言語に変換をすることができる。

また、Pandoc や Marp, SATySFi などを用いれば高品質な PDF を生成することも可能である。ツールを使うと様々なことができる。 

最近の技術系プラットフォームでは Markdown 記法をサポートしているものが多い。（GitHub, Discord, Qiita など）そのため、Markdown はプログラミングを学ぶ上では知っておいて損はない。

### Markdownのメリット

- HTMLなどと比べ、とても簡潔に書くことができる。
-  覚えやすい記述方式である。
- 数式や表などを入力できる。

などが挙げられる。

## 補足 : HTMLについて

- HTMLはHyperText Markup Languageの頭文字をとったもの。

- ウェブサイトの構造を記述する言語

- でも書くのが結構面倒くさい

このスライド:
```html
<h1> 補足: HTMLについて </h1>
<ul>
  <li> HTML... </li>
  <li> ウェブサイトの... </li>
  <li> でも書くのが... 面倒 </li>
</ul>
```

## 補足 : $\LaTeX$ について

- 組版ソフトウェア。組版は文字を組んでくれるってこと。

- これも結構書くのが面倒くさい（個人的な意見ですが。。。）

- でも式がきれいに書ける＋枯れているので技術的保証がある。

構文とかが気になる人は自分で見てみてね。

参考サイト:[TeX Wiki](https://texwiki.texjp.org/)

# Markdown の記述方法

以下、実際の表示を上に、記法を下に示している。

## 見出し

h1 と h2 は主に見出し

h3とh4はレポートの中で節とかを記述するときに使う。

h5とh6 はあんまり使わない気がする…

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

### h4

```
#### h4
```

##### h5

```md
##### h5
```
###### h6

```md
###### h6
```

## 段落

空の行を 1 段挿入する。もしくは半角スペースを文末に 2 つ挿入することでも改行できる。

東京理科大学

電子計算機  
研究会

```
東京理科大学
[空]
電子計算機__
研究会
```

## 区切り線

3 種類あるが、出力結果はすべて同じである。

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

半角ハイフン ( - )  + スペース + 内容

- RICORA

```
- RICORA
```

## 引用

半角大なり ( > ) を記述する。途中で ( > ) を増やすことにより 2 段引用が可能だ。
> Markdown（マークダウン）は、文書を記述するための軽量マークアップ言語のひとつである。本来はプレーンテキスト形式で手軽に書いた文書からHTMLを生成するために開発されたものである。
>  > Wikipediaより

```
> Markdown（マークダウン）は、文書を記述するための軽量マークアップ言語のひとつである。本来はプレーンテキスト形式で手軽に書いた文書からHTMLを生成するために開発されたものである。
>  > Wikipediaより
```

## リンク
説明とリンクをそれぞれ角括弧、丸括弧で書く。

[RICORA アルゴリズム班](https://alg.tus-ricora.com/)

```
[RICORA アルゴリズム班](https://alg.tus-ricora.com/)
```

##  画像

リンクの記述に感嘆符をつける。

```
![説明](URL)
```
![RICORA](https://avatars.githubusercontent.com/u/33452053)
```
![RICORA](https://avatars.githubusercontent.com/u/33452053)
```

## 数式

```＄＄```(本来は半角のドルマーク)で囲った間に $\TeX$ 記述をすれば表示される。

$\left(\bigcap_{i=1}^\infty\bigcup_{j=i}^\infty A_j\right)=0$

```
$\left(\bigcap_{i=1}^\infty\bigcup_{j=i}^\infty A_j\right)=0$
```

## 表

1行目に列名、二行目に揃え方、三行目以降にデータを入力。
 
|指定なし|中央揃え|右揃え|左揃え|
| - | :-: | -: | :- |
|あ|い|う|え|

```
|指定なし|中央揃え|右揃え|左揃え|
| - | :-: | -: | :- |
|あ|い|う|え|
```

## ソースコード

\```で文字を囲うことによりコード記述になる。インテンドでも代用ができる。

```C++
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

    aaa
    aaa


また、埋め込むことも可能だ。

例えば、`print('Hello, world!')`


    ``` C++
    #include <iostream>
    int main() {
      std::cout << "Hello、 World!" << std::endl;
      return 0;
    }
    ```

            aaa
            aaa


    `print('Hello, world!')`
