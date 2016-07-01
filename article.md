#Re:主要なプログラミング言語n種を解説
## はじめに

まあ元記事書いた人々の意図とは外れますが、重箱の隅をつついていきましょう。

## C言語

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>C言語はおそらくプログラミングの歴史上一番古く、プログラミングの基盤と言ってもいい言語です。

これにはこのコメントを。

>http://b.hatena.ne.jp/entry/292646265/comment/ockeghem  
>わかる。COBOL、FORTRAN、PL/I、LISP、ALGOL等は有史以前の言語ということですね

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>なぜC言語でOSを作る必要性があるかというと、C言語は数あるプログラミング言語の中でも最速の処理速度を誇るからです。

そもそも、OSが起動する際にはハードウェアに直接関わるような処理を記述する必要があります。  
(参考→[C++でできる！OS自作入門](http://www.slideshare.net/uchan_nos/cppos))  
そのため、直接機械語命令を使用できる[アセンブリ言語](https://ja.wikipedia.org/wiki/%E3%82%A2%E3%82%BB%E3%83%B3%E3%83%96%E3%83%AA%E8%A8%80%E8%AA%9E)で当初書かれました。しかし、アセンブリ書くのは面倒だ！ということでC言語が作られました。ですから、その説明では原因と結果が逆ですね

ついでにいうと、FORTRANとかC++だって速いです。逆にCだってフレームワークの性能などの理由により、常に最速とは限らないですし、コンパイラの最適化を阻害する書き方をすれば遅くなります。

(参考→[プログラミング言語の速度とアプリケーションの速度がいかに関係ないかがわかるグラフ](http://d.hatena.ne.jp/kwatch/20100430/1272585083))

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>学習する際は、歴史が古い分、図書館にC言語の学習書が豊富に並んでますので、学習素材には困りません。

なおまともな本は少ない模様。

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>まあボンクラがアセンブリ言語を書くよりはCで書くほうがよほどマシでしょうが、エキスパートがアセンブリ言語で書く場合はCより速くなることはママあります。コンパイラよりも最適なコードが書けないというのは、単にプログラマの能力が足りないんです。

んなこたーない。テメーのCの書き方が糞なだけだろ。今日のコンパイラは十分に優秀で、ちょっとやそっとではコンパイラに勝つことはできない。

>現在のアセンブリの利用例 | 本の虫  
>https://cpplover.blogspot.jp/2013/04/blog-post.html  
>結論として、ほとんどのパッケージで、ARMのための移植作業は必要ない。Ubuntuのレポジトリで言えば、アセンブリを利用しているパッケージは、全体のたったの6%だからだ。アセンブリを利用している多くのパッケージも、そのまま動く。移植性の高い高級なコードでの実装とパフォーマンス目的のアセンブリ実装を切り替えるようになっていたりするからだ。また、ほとんどのアセンブリ利用は、それほど価値がない。本来アセンブリで書かなくてもいいような処理までアセンブリで書いていたりするからだ。 

>C++標準化委員会の文書 2015-04-pre-Lenexaのレビュー: N4450-N4459 | 本の虫  
>https://cpplover.blogspot.jp/2015/06/c-2015-04-pre-lenexa-n4450-n4459.html  
>開発者へ：アセンブリを捨てろ。そんなに最適化できないし、そもそもコードを書いている時点で存在するアーキテクチャにしか対応できない。コンパイラーのパフォーマンスが期待通りでないのならばバグ報告を投げろ。標準化委員会に同期と並列実行を実現できる方法を提案しろ。ThreadSanitizerのようなツールをｔ受かってコード中の競合を発見しろ。 

>コンパイラーを負かす | 本の虫  
>https://cpplover.blogspot.jp/2015/03/blog-post_30.html  
>Pythonや、その他の動的型付け言語は、十分に速いかもしれないが、速いことは常にいいことだ。Cのような低級言語で速度を稼げるかもしれないし、アセンブリを手書きすることでもう少し上を行けるかもしれないが、コンパイラーを信頼したほうがいい。しかし、もし大量の12bitの数値を限りなく高速に足し合わせたいのであれば、まあ、これが答えだ

---

>https://toiroha.jp/article/detail/32380  
>オブジェクト指向言語ではないので、最近の主流の言語から比べると少し時代遅れの感があります。（C++はC言語にオブジェクト指向を拡張したものです）

C++はC言語にオブジェクト指向を拡張したものではないし、C言語はC++の下位にある言語ではありません。全くの別言語です

## C++

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>Cとほとんどの部分で共通しており、C++はC言語の上位互換です。

C++は、**断じて**C言語の上位互換ではありません。

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>例えばC言語ではコメントは/*～*/しか使えませんが、C++では//が使えます。

C99よりC言語でも使えます。

>http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1570.pdf  
>§6.4.9 Comments  
>2 Except within a character constant, a string literal, or a comment, the characters ``//``
introduce a comment that includes all multibyte characters up to, but not including, the next new-line character. The contents of such a comment are examined only to identify multibyte characters and to find the terminating new-line character.

## Java

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>JavaはAndroidアプリを開発する際に必要な言語です。

んなことはない。Android NDK（Native Development Kit）がなんのためにあるんだ。

あと、AndroidのJavaはJavaじゃない、みたいな話も有りましたね

Javaと偽Javaの話。 - なるようになるかも
http://quesera2.hatenablog.jp/entry/2016/05/28/180834

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>C言語に匹敵する処理速度を誇り

[Java](https://ja.wikipedia.org/wiki/Java)は元々、プラットフォームに依存せず扱いやすい言語を目指して開発されました。[Javaアプレット](https://ja.wikipedia.org/wiki/Java%E3%82%A2%E3%83%97%E3%83%AC%E3%83%83%E3%83%88)から始まったその発展は、クライアントやサーバー、パソコンや組込み機器など多岐に渡ります。  
[Android OS](https://ja.wikipedia.org/wiki/Android)用のソフト開発に使われるのは主にC/C++かJavaですが、前者のアプリはネイティブで実行され、後者は[Dalvik仮想マシン](https://ja.wikipedia.org/wiki/Dalvik%E4%BB%AE%E6%83%B3%E3%83%9E%E3%82%B7%E3%83%B3)(Android 4.4以前)か[ART仮想マシン](https://ja.wikipedia.org/wiki/Android_Runtime)(Android 4.4以降)で実行されます。  
昨今では、[Xamarin.Android](http://www.xlsoft.com/jp/products/xamarin/platform.html)によって[C#](https://ja.wikipedia.org/wiki/C_Sharp)でもAndroidアプリを開発できるようになりました。  
なお、「ソースコードから生成したバイトコードを仮想マシン(VM)上で動かす」性質上、速度は比較的遅い方です。

## JavaScript

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>JavaScriptはWebページを作成する際に必要な言語です。

たしかによく使われていますが、なくたって作れます。

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>例えば、jQueryはJavaScriptのプラグイン。つまりJavaScriptによって書かれた便利な機能をjQueryの簡単な文法を使うことで気軽に利用出来るものです。

何を言っているのかわからないんですがそれは・・・。jQueryはライブラリであって、文法やないで。

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>視覚的に組み込まれているのがJavaScriptの特徴

視覚的とは

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>JavaScriptは、C言語よりも歴史が古いLISP言語の影響を強く受けた関数型言語で

関数型言語と言うよりはプロトタイプベースのオブジェクト指向では？


## C#

## Ruby

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
> Rubyの特徴として、自由な点があります。

**もう少し詳しく書いてくれないとツッコむ部分がないではありませんか(暗黒微笑)**

## PHP

## Python

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
> AI(人工知能)にプログラミング言語を組み込むことで

プログラミング言語で機械学習を実装するのでは……？

## Swift

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
> Swiftは、Appleが開発したiPhoneアプリを開発する際に必要な言語です。

**[Xamarin.iOS](http://www.xlsoft.com/jp/products/xamarin/platform.html)がアップを始めました。**