# Re:主要なプログラミング言語n種を解説
主要なプログラミング言語n種を解説！の類に反論するためのネタリポジトリ。

## 参考記事
[主要なプログラミング言語 5種類を徹底解説!](http://cpg.hatenablog.com/entry/2016/06/30/193755)  
※修正前(WebArchive収録)の分については、既に修正されていることから扱わないことにする

## ツッコミどころまとめ

> なぜC言語でOSを作る必要性があるかというと、C言語は数あるプログラミング言語の中でも最速の実行速度を誇るからです。

そもそも、OSが起動する際にはハードウェアに直接関わるような処理を記述する必要があります。  
(参考→[C++でできる！OS自作入門](http://www.slideshare.net/uchan_nos/cppos))  
そのため、直接機械語命令を使用できる[アセンブリ言語](https://ja.wikipedia.org/wiki/%E3%82%A2%E3%82%BB%E3%83%B3%E3%83%96%E3%83%AA%E8%A8%80%E8%AA%9E)や、直接メモリを操作できる[C言語](https://ja.wikipedia.org/wiki/C%E8%A8%80%E8%AA%9E)が必要になるのです。  
なお、C言語は**適切に書けば**高速な実行速度を叩き出しますが、フレームワークの性能などの理由により、常に最速で入られるとは限りません。  
(参考→[プログラミング言語の速度とアプリケーションの速度がいかに関係ないかがわかるグラフ](http://d.hatena.ne.jp/kwatch/20100430/1272585083))

> JavaはAndroidアプリを開発する際に必要な言語です。
> (中略)
> C言語に匹敵する処理速度を誇り

[Java](https://ja.wikipedia.org/wiki/Java)は元々、プラットフォームに依存せず扱いやすい言語を目指して開発されました。[Javaアプレット](https://ja.wikipedia.org/wiki/Java%E3%82%A2%E3%83%97%E3%83%AC%E3%83%83%E3%83%88)から始まったその発展は、クライアントやサーバー、パソコンや組込み機器など多岐に渡ります。  
[Android OS](https://ja.wikipedia.org/wiki/Android)用のソフト開発に使われるのは主にC/C++かJavaですが、前者のアプリはネイティブで実行され、後者は[Dalvik仮想マシン](https://ja.wikipedia.org/wiki/Dalvik%E4%BB%AE%E6%83%B3%E3%83%9E%E3%82%B7%E3%83%B3)(Android 4.4以前)か[ART仮想マシン](https://ja.wikipedia.org/wiki/Android_Runtime)(Android 4.4以降)で実行されます。  
昨今では、[Xamarin.Android](http://www.xlsoft.com/jp/products/xamarin/platform.html)によって[C#](https://ja.wikipedia.org/wiki/C_Sharp)でもAndroidアプリを開発できるようになりました。  
なお、「ソースコードから生成したバイトコードを仮想マシン(VM)上で動かす」性質上、速度は比較的遅い方です。

> Rubyの特徴として、自由な点があります。

**もう少し詳しく書いてくれないとツッコむ部分がないではありませんか(暗黒微笑)**

> AI(人工知能)にプログラミング言語を組み込むことで

プログラミング言語で機械学習を実装するのでは……？

> Swiftは、Appleが開発したiPhoneアプリを開発する際に必要な言語です。

**[Xamarin.iOS](http://www.xlsoft.com/jp/products/xamarin/platform.html)がアップを始めました。**

> その他日本語の文法的に怪しい箇所

**校正しましょう。**

