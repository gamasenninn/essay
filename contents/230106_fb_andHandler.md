# 近況報告　ー　業務開始

今年最初の業務  

初仕事  

デバイスへClaim成功したところまでで  
年末の仕事収めになったのじゃが  

新年あけての仕事はじめの本日は  
RFIDからのID読み込みなのじゃ  

IDタグ読み込みを開始し  
コールバックで受信処理をする  
受信したデータをMAPで切り刻んで  
画面のListViewにリアルタイム表示する  
ってとこまでやった  

androidの特性上、コールバック先からは  
直接画面をいじれないわけで  
無理やりぶち込むと、エラーもしくは  
だんまりになってしまう  
それを解決するには  
スレッドをたててhandlerを作ったうえで  
handler経由で画面を更新する  
というフローになる  

この部分をflutterに橋渡しできればよいのじゃが  
このリアルタイム処理部分が  
かえって面倒になってしまう  
どうしたものか考えどころだが  
まあいずれにしても、  
kotlinのネイティブ部分とRFIDの接続構造を  
もっと深く精査する必要があるのは間違いない  

とりあえず  
RFIDのリアルタイム取り込みまで成功したので  
今日はここまでとする  
  

