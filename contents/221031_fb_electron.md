 
# 近況報告　-　JavaScript/TypeScriptをなめたらあかん  
  
ITエンジニア諸君!!  
VSCode使ってますか？  
ワシは使ってます  
   
github連携を前提にした開発では  
なくてはならないエディターですね  
最初のころはAtomを使っていたが  
弟子と共同作業する必要があり  
VSCodeに嫌々切り替えたのだが・・・・  
いまでは何をするにもVSCodeしか使わなくなったよ  
軽いし、欲しい機能をすぐにアドインして使えるし  
カスタマイズの自由度が高いし  
まるで魔法のようなエディターだ  
  
このエディター、なんの言語で書かれているか知ってるかい？  
C++ ?  
C# ?  
Go ?  
Rust ?  
立ち上がりも速いし、サクサク動くし、  
当然コンパイラ言語で書かれてると思うよね  
  
正解は  
TypeScript(JavaScript上位互換言語)です。  
知っている人はあたりまえじゃんと思うかもだが、  
知らない人はまずビックリする。  
「なんでJavaScript/TypeScriptみたいなオモチャ言語であそこまでできるんだ？」  
ってね  
  
わかるよ、わかるけどね  
もうね、そういう発想自体が昭和なんよ  
若くして老害なんよ  
  
あるときnode.jsという彗星がIT界に降ってきたときから  
Webの世界はガラリと変わったんだよ  
サーバーサイドでJavascriptが動くようになり  
ファイルIOやDB連携など  
ほぼすべてのことができるようになった
WebのHTTPサーバとしては  
ノンブロッキング・シングルスレッドで  
C10K問題(1万台からのアクセスは可能か)
があっさり解消され  
その優秀さが明るみになり  
マルチスレッド、マルチプロセスの価値が半減した  
  
node.jsの出現により  
フロントエンドからバックエンドに至るまで  
JavaScriptだけでWebプログラミングが  
完結できてしまうようになったのさ  
それによってJavaScriptは  
事実上Web技術の言語としてメインストリームにのし上がった  
  
そしてまたあるとき、electronというフレームワークが  
ひっそりと生まれた  
一言でいえば小さなwebブラウザを
ラインタイム的に搭載したもので  
もちろんnode.jsと連携できる  
これによってローカルファイルの読み書きも  
低レイヤ層のリンクも可能になった  
もっと簡単にいえば何でもできる小さなブラウザってことだね  
これがwindows、mac、Linux上でサクサク動くのだよね  
だから、このワークフレーム上で作られたものは  
当然ながらローカル環境上で動き  
マルチプラットホーム化できる  
しかもJavascript+HTML+CSSだけで  
デスクトップアプリをつくることができわけさ  
  
このフレームワークでgithub社によって作成されたのが  
「Atom」というエディターだ  
Atomはeclipse同様、すべてのプラットホームで動くエディターで  
軽く、アドオン（拡張機能）が豊富  
githubとの連携が簡単にできるなどで  
エンジンアやデザイナーへの浸透は比較的早かった  
  
そして、electronをフレームワークとして
Visual Studio Code（VSCode）という神アプリが登場する  
機能の説明は特に必要ないだろう  
Atomユーザをすべてといってよいほど食らい付くした  
そして、Atomの役目は終了しメンテナンスモードに移行した  
  
オープンソースという点でもすごい  
スター数（いいね数）が約14万件、  
フォーク数（継承数）が24000件  
コントリビュータ数（開発協力者数）が1723人  
まさに化け物のようなオープンソースプロジェクトだ  
ソースを覗いてみると  
ほとんどのファイルが.ts、.jsではないか  
Languagesの項目をみるとなんと  
TypeScript 93.5%  
JavaScript 3.0%  
なので本当にびっくりする  
  
気がついたら
周りはJavaScriptに包囲されていた  
VueもReactも  
GAS(Google App Script)も  
KIintoneカスタマイズも  
React NativeもCordovaも  
みんな、みんなJavaScriptで書くのだった・・・  
  
さて、これでも  
Javascript/Typescriptはおもちゃ言語といえるだろうか？  
Web技術ではダントツにJavascript/Typescriptが必須であることが  
わかっていただけただろうか？  
なにもコンパイラ言語だけが言語ではなく  
C++でプログラミングができたとしても  
JavaScriptを使えないというのは  
ITエンジニアとして致命的欠落といえる時代になってしまったのだ  
  
エンジニア諸君  
自信をもってJavaScriptを学ぼう  
ちなみにわしの言語順の使用頻度は次のとおりである  
1.  JavaScript/TypeScript
2.  python
3.  PHP
4.  HTML/CSS
5.  VBA
6.  Go
7.  kotlin(Java)
  
pythonistaなのに、  
なぜかしら使用頻度が一番高いのがJavaScript  
これは意識したのではなく  
Web開発をしていたら  
自然にそうなってしまったのだ  

この中で、最終的にはVBAとPHP部分を  
別言語に移行する予定であるが  
そのときは、おそらくpythonかJavaScriptになるだろう  
見ての通りワシが一番好きだったC系の言語は  
いまでは全く書いていない  
  
  
https://github.com/microsoft/vscode  
