#  近況報告 - 非同期地獄の中の蜘蛛の糸 - 状態遷移表  

プログラマーの諸君  
状態遷移表書いたりしてる？   

え？
-  それはSEとかPMの仕事だから書かない？
-  状態遷移表ってなに？
-  知ってるけど書かないなあ
-  いまどき流行らんだろそんな昔の手法  

知らない人のためにいうけど  
「状態」と「イベント」の相関を  
一枚の表にしたもの  
詳しくはググってくれ    
とても簡単なものだから    
優秀な君たちならすぐに理解できるだろう    
  
ここでは  
知っているか知っていないかを問題にしていない  
モダンな手法か古い手法かなんかも問題にしていない  
書くか書かないかだけを聞いているんだけね    
  
もちろん普段はプログラマーが書かなくてもいい代物だが  
なにかあったときに  
すさまじい威力を発揮してくれる    
  
機械制御系のエンジニアの間では  
通信プロトコルを定義したり  
機械制御の仕様を書く場合とか  
かならず必要なものだった 
過去形でいっているのは  
ワシが機械制御系SEをやっていたのは  
35年も前のことだから・・・・ 
  
Web系エンジニアの間では  
あまり流通していない設計手法かもしれない  
だが、これ  
設計の段階でだけなく    
プログラミングの段階でも有効なものだ    
  
昨今、Web系の仕事に非同期処理は当たり前  
つうか、非同期処理がないWebシステムは存在しないだろう
非同期ロジックを実装する場合  
状態とイベントの相互の関係を理解するのは必須であり  
通常、プログラマーはそれを自分の頭の中でやっている  
しかも、そのへんの仕様書は存在せず  
プログラマーに丸投げしていることのほうが多い  

・・・この状態のとき、Aボタンが押されたときこのAPIを呼ぶ、と  
正常なら状態Bに移るけどコールバックでデータ表示させて、  
エラーが起きたら、トースト表示して、と  
あれ、まてよ、リトライしなくていいんだけ？  
タイムアウトどうするんだっけ？  
めんどうだから全部awaitでいいか・・・

・・・など、頭の中では  
状態とイベントの図のようなものが自然にできあがる  
しかし、それだと、あり得ないイベントを拾ったとき  
どのような処理、どのような状態に遷移するのか  
複雑になってくると君の頭は
簡単にオーバーフローしてしまう    
  
こんなとき、状態遷移表が威力を発揮するのだ  
正常系だけなら必要はない  
だが異常系、あり得ない系には
これがあるか、ないかで雲泥の差となる  
  
そして、極めつけのポイントは   
「あり得ないこと」  
「何もしないこと」  
を明確にすること  
不可と無視を可視化できる  
これが大きなメリットだ    
状態遷移図だとこれができないし  
君たちの頭の中では、ケースすべてを網羅するには  
メモリが足らなすぎる  
なので、表でまとめるわけさ  
（手書きでもエクセルでもなんでもいい ）
  
これは、設計段階以外、  
プログラミングをする場合でも実はすごく有効で    
これを書く過程であらゆるケースが整理されてくる  
最後のころには  
非同期地獄から開放される感覚になるだろう  
そして  
テストプログラムを書くときに  
この表のケースを機械的に網羅すればよい  
嘘のようにロジックが強くなっていくのが実感するだろう  
  
書くべきか書かざるべきか  
なんて迷う必要はない  
状態とイベントで迷ったらとりあえず書いてみる  
非同期地獄の中で迷子になったらとりあえず書いてみる  
それだけだ  

