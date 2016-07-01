# Re:主要なプログラミング言語n種を解説
## はじめに

このリポジトリは、「主要なプログラミング言語n種を解説」といった類の記事を斬るためのものです。対象とする記事はこちら。

- [主要なプログラミング言語 5種類を徹底解説! - Programming share](http://cpg.hatenablog.com/entry/2016/06/30/193755)
- [主要なプログラミング言語8種をざっくり解説 - shi3zの長文日記](http://d.hatena.ne.jp/shi3z/20160701/1467330446)
- [2015年の人気プログラム言語６つを徹底比較！気になる年収や求人、学習難易度まで｜トイロハ](https://toiroha.jp/article/detail/32380)

## C言語

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>C言語はおそらくプログラミングの歴史上一番古く、プログラミングの基盤と言ってもいい言語です。  
>**(編者注：現在は削除された文面です)**

これについては、次のコメントを貼るだけに留めます。

>http://b.hatena.ne.jp/entry/292646265/comment/ockeghem  
>わかる。COBOL、FORTRAN、PL/I、LISP、ALGOL等は有史以前の言語ということですね

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>なぜC言語でOSを作る必要性があるかというと、C言語は数あるプログラミング言語の中でも最速の処理速度を誇るからです。

OSをプログラミングする際には、ハードウェアに直接関わる処理を記述する必要があります。  
(参考→[C++でできる！OS自作入門](http://www.slideshare.net/uchan_nos/cppos))  
そのため、当初は機械語命令と一対一対応する[アセンブリ言語](https://ja.wikipedia.org/wiki/%E3%82%A2%E3%82%BB%E3%83%B3%E3%83%96%E3%83%AA%E8%A8%80%E8%AA%9E)によってOSが記述されていました。  
しかし、機械語はそれを動かすCPUによって仕様が異なるため、他のハードに移植する際に酷く苦労することになりました。  
そこで、ハードウェアに関わるような処理を記述できる上、より移植性が高いコードを書くことができる[C言語](https://ja.wikipedia.org/wiki/C%E8%A8%80%E8%AA%9E)が誕生しました。  
したがって、正しい順番としては**「C言語→OS」ではなく「OS→C言語」**ということになります。

ちなみに、速度面で言えば理論上は機械語＝アセンブラが最速……ですが、  
実際にはコンパイラや使用するフレームワークの性能などにより**幾らでも変化します**。  
(参考→[プログラミング言語の速度とアプリケーションの速度がいかに関係ないかがわかるグラフ](http://d.hatena.ne.jp/kwatch/20100430/1272585083))

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>学習する際は、歴史が古い分、図書館にC言語の学習書が豊富に並んでますので、学習素材には困りません。

C言語は、開発人口の多さと規格内の未定義・処理系依存部分が多いことなどから、**学習書に間違いが書かれている**ことが珍しくありません。  
そのため、冗談抜きで**「迷ったら規格書を読め」**と勧められることがままあります。  

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>まあボンクラがアセンブリ言語を書くよりはCで書くほうがよほどマシでしょうが、エキスパートがアセンブリ言語で書く場合はCより速くなることはママあります。コンパイラよりも最適なコードが書けないというのは、単にプログラマの能力が足りないんです。

近年のコンパイラは優秀ですので、手動でガリガリとアセンブリを書くよりずっと高速になることが多いです。  
そもそも、プログラミングの原則として**「[最適化するな](http://d.hatena.ne.jp/foursue/20060629/p1)」**といのがあるぐらいですしね……。

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

C++はC言語にオブジェクト指向を拡張したもの**ではありません**し、C言語でもオブジェクト指向はできます。  
C++について言えば、もちろんオブジェクト指向もできますが、それ以外にも[template](http://qiita.com/narumi_/items/f656678c78d50c40bc1c)など様々な機能が拡張されています。  
また、C言語もC言語で**独自の発展**を遂げ、またコーディングスタイルは全く異なるものになりましたので、**C++の下位互換というのは誤った認識**かと思われます。

## C++

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>Cとほとんどの部分で共通しており、C++はC言語の上位互換です。

前述したように、C++は**断じて**C言語の上位互換ではありません。

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>例えばC言語ではコメントは/*～*/しか使えませんが、C++では//が使えます。

C言語でも、C99から``//``コメントが使えるようになりました。

>http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1570.pdf  
>§6.4.9 Comments  
>2 Except within a character constant, a string literal, or a comment, the characters ``//``
introduce a comment that includes all multibyte characters up to, but not including, the next new-line character. The contents of such a comment are examined only to identify multibyte characters and to find the terminating new-line character.

## Java

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>JavaはAndroidアプリを開発する際に必要な言語です。

**[Android NDK](http://qiita.com/alingogo/items/203477c9da373ab7eacb)がアップを始めました。**  
(※NDK＝Native Development Kitとは、C++などでネイティブコードを書くためのキットのこと)  
また、AndroidのJavaは**正式なJavaではない**、といった話が以前飛び交いましたね……。  
(参考→[Javaと偽Javaの話。](http://quesera2.hatenablog.jp/entry/2016/05/28/180834))

昨今では、[Xamarin.Android](http://www.xlsoft.com/jp/products/xamarin/platform.html)によって[C#](https://ja.wikipedia.org/wiki/C_Sharp)でもAndroidアプリを開発できるようになりました。  

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>C言語に匹敵する処理速度を誇り

[Java](https://ja.wikipedia.org/wiki/Java)は元々、プラットフォームに依存せず扱いやすい言語を目指して開発されました。[Javaアプレット](https://ja.wikipedia.org/wiki/Java%E3%82%A2%E3%83%97%E3%83%AC%E3%83%83%E3%83%88)から始まったその発展は、クライアントやサーバー、パソコンや組込み機器など多岐に渡ります。  
[Android OS](https://ja.wikipedia.org/wiki/Android)用のソフト開発に使われるのは主にC/C++かJavaですが、前者のアプリはネイティブで実行され、後者は[Dalvik仮想マシン](https://ja.wikipedia.org/wiki/Dalvik%E4%BB%AE%E6%83%B3%E3%83%9E%E3%82%B7%E3%83%B3)(Android 4.4以前)か[ART仮想マシン](https://ja.wikipedia.org/wiki/Android_Runtime)(Android 4.4以降)で実行されます。  
なお、「ソースコードから生成したバイトコードを仮想マシン(VM)上で動かす」性質上、速度は**比較的遅い方**です。

---

>https://toiroha.jp/article/detail/32380  
>Javaは成熟した傾向があり、最近の主流の言語から置いていかれた傾向があります。そのため、あまり新しい機能が追加されることが少ないです。

[Java 7](http://aoking.hatenablog.jp/entry/20110808/1312769605)・[Java 8](http://qiita.com/oohira/items/9c13f92815266cc5112c)が登場しましたので、まだ**進化の余地を残している**かと。

## JavaScript

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>JavaScriptはWebページを作成する際に必要な言語です。

確かによく使われていますが、必須というほどでもありません。どちらかと言えば[HTML](https://ja.wikipedia.org/wiki/HyperText_Markup_Language)に当てはまる言葉でしょう。

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>例えば、jQueryはJavaScriptのプラグイン。つまりJavaScriptによって書かれた便利な機能をjQueryの簡単な文法を使うことで気軽に利用出来るものです。

「jQueryの文法」とは一体何なのでしょうか。  
確かに独特な記法をよく使用しますが、それらは全て[JavaScript](https://ja.wikipedia.org/wiki/JavaScript)によって作られたものであり、原理上は全てJavaScriptで記述することができます。

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>視覚的に組み込まれているのがJavaScriptの特徴

「視覚的」とは、一体どういった意味なのでしょう？

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>JavaScriptは、C言語よりも歴史が古いLISP言語の影響を強く受けた関数型言語で

確かに[クロージャ](http://qiita.com/takeharu/items/4975031faf6f7baf077a)の機能は存在しますが、実際には[プロトタイプベースのオブジェクト指向言語](http://qiita.com/takeharu/items/809114f943208aaf55b3)として使用されることが多いのではないでしょうか。

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>V8やnodeJSを使えばサーバーサイドのプログラミングも可能です。

V8では出来ないと思われます。

## Ruby

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
> Rubyの特徴として、自由な点があります。

**もう少し詳しく書いてくれないとツッコむ部分がないではありませんか(暗黒微笑)**

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>最近のはJITが入ってVM化して速くなったそうですが

RubyのJIT化はRuby 3.xに向けた実験段階だったかと。  
(参考→[Ruby 3.0の未来へ―、言語設計者のまつもと氏が示す3つの方向性とRuby哲学](http://hrnabi.com/2015/05/12/7035/))

---

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>DHHというオランダ人を

DHH([デイヴィッド・ハイネマイヤー・ハンソン](https://ja.wikipedia.org/wiki/%E3%83%87%E3%82%A4%E3%83%B4%E3%82%A3%E3%83%83%E3%83%89%E3%83%BB%E3%83%8F%E3%82%A4%E3%83%8D%E3%83%9E%E3%82%A4%E3%83%A4%E3%83%BC%E3%83%BB%E3%83%8F%E3%83%B3%E3%82%BD%E3%83%B3))さんはデンマーク人ではないかと。

## PHP

>http://d.hatena.ne.jp/shi3z/20160701/1467330446  
>PHPはApacheと一体化してるので

これについても、次のコメントを貼るだけに留めます。

>http://b.hatena.ne.jp/entry/292721861/comment/living  
>「PHPはApacheと一体化してる」mod_phpも使ってるけど、パフォーマンスを求める場合はPHP-FPM（要はFastCGI）の方が多いと思う

## Python

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
> AI(人工知能)にプログラミング言語を組み込むことで

プログラミング言語で機械学習を実装するのでは……？

---

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
>その際に必要な言語がPythonです。

機械学習に使用されるライブラリを記述する言語としては、**主にC++が使われます**。  
その理由としては、**莫大な計算量を**(特に学習に)**要するので速いほうがいい**といったことがあります。  
また、機械学習を利用するコードについては様々な言語が利用可能です。  
例えば、ディープラーニングによる画像処理で有名な[waifu2x](http://kourindrug.sakura.ne.jp/waifu2x.html)は、PythonだけでなくC++・HSP・JavaScript・Rustなど様々な言語で実装されています。  

もっとも、Pythonには豊富なライブラリがあることから、(機械学習を含めた)数値計算や画像処理などを簡単に記述することができます。  
したがって、機械学習に触れる際にPythonも学ぶのは良い選択肢かと。

## Swift

>http://cpg.hatenablog.com/entry/2016/06/30/193755  
> Swiftは、Appleが開発したiPhoneアプリを開発する際に必要な言語です。

**[Xamarin.iOS](http://www.xlsoft.com/jp/products/xamarin/platform.html)がアップを始めました。**