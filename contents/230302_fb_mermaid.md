# chatGPT －　chatGPTで作図したい場合はmermaidを使う

chatGPTの答えを図にしたい  
と思う人は多いだろう  
そういうときは、
一旦、何らかのスクリプト形式で出力してもらうとよい  
おすすめはmermaid記法のドキュメントである  
シーケンス図、ガントチャート、ER図など  
さまざまな書式がある  

mermaid記法で書いたドキュメントは  
NotionやVsCode、githubなどで表示できる  

写真の図は、  
mermaid記法で  
chatGPTにER図のサンプル、  
ガントチャートのサンプル及び  
auth2.0のシーケンス図サンプルを出力依頼したもの  

 
```mermaid
erDiagram
    customer ||--o{ order : places
    order ||--|{ order_item : contains
    customer {
        string name
        string email
        string phone
    }
    order {
        string order_id
        date order_date
    }
    order_item {
        string item_id
        integer quantity
        decimal price
    }

```

``` mermaid
gantt
    title ガントチャート
    dateFormat YYYY-MM-DD
    section セクション1
    タスク1          :done,    des1, 2023-03-01,2023-03-03
    タスク2          :active,  des2, 2023-03-04, 3d
    タスク3          :          des3, after des2, 5d

```

``` mermaid
sequenceDiagram
    participant User
    participant Client
    participant AuthorizationServer
    participant ResourceServer

    User->>Client: リソースの要求
    Client->>AuthorizationServer: 認可要求
    AuthorizationServer->>User: 認可のリクエスト
    User->>AuthorizationServer: 認可の許可
    AuthorizationServer->>Client: 認可グラント
    Client->>AuthorizationServer: アクセストークンのリクエスト
    AuthorizationServer->>Client: アクセストークン
    Client->>ResourceServer: リソース要求
    ResourceServer->>Client: リソースのレスポンス
```