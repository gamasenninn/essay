#  近況報告 - gitレポジトリは萌えているか？  
  
gitを導入していないシステム開発会社って存在しますかね？    
実はいまだに存在するんです  
令和を生きるエンジニアには信じられないことだと思う  
    
ワシのように一人で社内システムのプログラミングをしているものでも  
gitは必要だし、gitのリポジトリ管理も必要だ    
プロジェクトはまるっとすべてgithubで管理している  
そのうえでCI/CDパイプラインを少しずつ構築している  
    
チームでの開発ならわかるけど  
たったひとりなら  
-  ソースの履歴管理なんかいらんないじゃね？  
-  自動テストなんて無駄じゃね？  
-  ましてCI/CDパイプラインなんか構築する必要ないんじゃね？  
-  それより仕様書をまとめたほうがいいんじゃね？  
-  それより未消化タスクを消化したほうがいいんじゃね？  

などと思われるかもしれない  
  
だとしたら、その疑問を呈した人は  
なにもわかっていないバカプログラマー
もしくはバカエンジニアです  
（トラベルナース風にいってください）  
  
一人でプログラミングしているからこそ  
gitリポジトリ管理は必要なんです  
仕様書なんてくそくらえ、です  
仕様書書く暇あったらテスト書け、パイプライン書け、です  
（これもトラベルナース風に）  
    
一人のプラグラマーによって作られた社内システムが  
ちゃんと動いていたと仮定しよう   
なにも問題ないようにみえる  
システムは空気や水のように当たり前にそこにある  

でももしそのプログラマーが他の会社に転職したら？   
あるいはあまりに生意気なのでクビにしたいなら？  
最悪だが、死んでしまったら？   
そいつがいなくなったら、  
システムはたぶん誰もメンテナンスできないだろう   
その時点でシステムは死ぬ  
（システムは生き物だから）

だからこそ、  
gitリポジトリでソースを管理さえしていれば  
そしてCI/CDパイプラインが構築されていれば  
他の誰かがそれを引き継ぐことは可能となるのだ  
  
ワシのプロジェクトは  
汎用性のあるものはパプリック、  
機密性のあるものはプライベートとし
すべてのソース・ファイルをgithubに移行した  
だからたとえワシが死んでも、  
リポジトリを見て理解すれば  
誰でも引き継ぎは可能なようになりつつある  
  
だが、赤の他人が、どうやってシステムを理解するのか？  
普段からgithubを使っているエンジンにならすぐにわかることだ

たとえば・・・・・

それぞれのプロジェクトは誰のものであれ  
自然にgithub flowのように何らかのワークフローができてくる  
そのワークフローのクセさえ読み解けば  
システム全体が見えてくる  
    
なんらかのフレームワーク  
たとえばLaravelやDjango、Railsなど使っていれば  
その流儀にしたがってディレクトリが構成されているので  
アプリ全体のモデルがわかる  
フロントも同じく流儀にしたがって理解すればよい    
  
また、テストプログラム自体が仕様書のようなもので  
プロジェクトを読み解くには  
ユニットテストを覗けばすぐに
メソッドのパラータや使い方が読み解ける  
e2eテストを動かしてみれば  
システム全体がどうやって動いているのか一目瞭然  

swaggerの定義体があったら  
それこそ、それがAPIの仕様書  
（fastAPIは自動で出力）  

CI/CDパイプラインにしてもそう  
どんなコンテナでどんな処理を動かすか  
フローを覗けばそれがわかるため  
システムの環境変数とその設定  
起動方法や手順なども読み解ける  

というわけで、  
たとえばワシのシステムは  
-  githubちょっとできる  
-  dockerちょっとできる  
-  pythonちょっとできる  
-  テストプログラムちょっと書ける  
-  CIパイプラインちょっとわかる  
    
という条件が揃っていれば  
誰でも読み解くことはできる簡単なものであり  
ワシ死んだあとのメンテナンスも
地域に限定されないため  
CrowdWorksとか、Lancersとか  
リモートで作業してくれるエンジニアを地球上から探せばよいだけだ  
なんなら、プログラミング初心者でも  
この条件をクリアできる学習さえしてもらえば    
だれでもメンテナンスできるのだ  
そしてパイプラインを維持しさえすれば  
継続的インテグレーションは可能になる  
  
地域のSIerに開発依頼するしかないと思っていないか？  
　　  
「仕様書さえあればメンテナンスできます」  
「仕様書がないので、読み解き工数含めて20人月ですね」  
「この地域ではこのシステムを理解して再構築できるのは当社だけです」  
  
そんなまことしやかな言葉に騙せれてはいけない  
中小零細企業では大手中小SIerが提示する金額なんて  
正当な見積もりだとしても  
はなっから出せやしないのだ  
  
どうしてもエンジニアのあてがない・・・  
ネットから探すのなんて怖いし、ちょ無理・・・・  
かといって
モダン開発ができる経験を積んだプログラマーを雇うなんて  
うちでは払えない（50万円～/月）  

　　　※ワシの場合は、プログラマーとしての単価ではなく  
　　　　業務作業員として通常バイトの単価なので  
　　　　まったく参考にならないからね  
  
ならば、育てよう  
未経験者でもよいから、ちょっとできるを目指し  
最初からgitリポジトリ上で  
エクストリーム・プログラミング(XP)を実施する  
先輩と後輩の、
あるいは師匠と弟子の  
あるいはメンターと生徒の  
コードレビューを定着させ  
OJTで育てるのだ  
中小零細企業だからこそモダン開発手法は社内で容易に導入できる  
という発想でいこう  
（だって導入障壁は最初から何もないだろ）  
  
gitはまさに解放軍の武器  
githubやgitlabは解放軍の基地  
OSSは解放軍そのもの  

旧態然としたSIerからの見積金額から自由になるため  
システムの継続的インテグレーションのため  
社内にDX革命を起こすため  
まあ、理由はなんでもいい  
    
git解放軍に参加しましょうぞ    
  
できればOSSでコミットしましょう      
できればドキュメントを英語でね  
できればISSUEも英語でね  
（苦手に思うことはないDeepLがついている）
  
gitリポジトリは萌えているか？  

※ちなみにワシのgithubの萌え具合は画像のとおり  
春の野原のような淡い萌え具合だが  
いちおう毎日コミットしてます  