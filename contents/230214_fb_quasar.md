# 近況報告　－　Vue3でComposit APIとQuasarでWebアプリ  

Vue2をVue3に変更しないとならんので
手始めに今つくっているラベルプリンター出力用のWebアプリを
Vue3でつくっているわけだが  
composit API + <script setup>
にするととてもよい

記述がシンプルになるし  
ソースの見通しがよくなり    
よりJavascriptコードよりの記述になり  
個人的にはOptions APIより気に入っている  

写真のようにサンプルを書いてみた

githubからユーザをリストを取得し  
リストに表示する
というシンプルなものだ  
Options APIと比較すると見通しがよいと思う  

フレームワークはQuasarを使っている  
Quasarならワンソースで  
electronのディスクトップアプリ化ができるし  
Webアプリもできるし  
スマホアプリもできる  
人的リソース不足のワシには
ピッタリのフレームワークである  

以下はTipsになるが  
webのビルドで生成されたdist/spa下のindex.htmlは  
クリックしただけではローカルで動かない場合が多い  
簡単なWebサーバーを起動して確認するとよい
以下の方法がある  

pythonの場合は、
  python -m http.server

npmの場合は、
  npm install -g http-server
  http-server

npxの場合は、
  npx serve

