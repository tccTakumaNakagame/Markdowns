# Google Cloud OnBoard
---

<!--
# Google Cloud OnBoardで学んだこと
- **Google Cloud Platform(GDP)の全体像**
    - Compute Engine
    - App Engine
    - Cloud Storage
    - Cloud Datastore
    - Cloud Bigtable
    - **Container Eingie**
    - 機械学習
-->

# Google Cloud OnBoard AGENDA
  - モジュール1 - Google Cloud Platformのご紹介
  - モジュール2 - Google Cloud Platformの入門
  - モジュール3 - Google App EngineとCloud Datastore
  - モジュール4 - Google Cloud Platformストレージオプション
  - モジュール5 - Google Container Engine
  - モジュール6 - Google Compute Engineとネットワーキング
  - モジュール7 ビックデータ
  - Google Cloud Platformの機械学習

# モジュール1 - Google Cloud Platformのご紹介
## 概要
  - GCPを選ぶ理由
  - Googleのインフラストラクチャ
  - 環境への取り組み
  - 顧客本位の料金体系
  - 次世代のクラウドコンピューティング
  - IaaSとPaaS
  - 各種サービス一例

 ## GCPを選ぶ理由
  一般のデベロッパーが、Googleの構築した最高の環境を、Google社員とほぼ同じように使うことが出来る。  
  - 高いスケーラビリティ、安全性、信頼性を確保  
  - ウェブ/モバイル/アナリティクス/バックエンドなど、様々な分野に特化した環境を提供

## Gogleのインフラストラクチャ
  - 全てのGoogle所有のデータセンター同士を専用線で接続
  - 海を超えた高速・セキュアなネットワークの利用が可能
  - 新設された東京リージョンは"AsiaNorthEast"

## 環境への取り組み
  - エコシステムを尊重しながらインフラストラクチャを開発
  - 再生エネルギーへ最大の投資
  - 初めてISO14001を取得したDC
  - 2007年以降、100%カーボンニュートラル

## 顧客本位の料金体系分単位の課金と長期割
  - 最初の10分固定+1分単位での課金
      - サービスごとの細かい費用を抑えることが出来る
      - 時間課金の場合
          - 10分：1時間分の料金
          - 61分：2時間分の料金
  - 同じ環境を使い続ければ、長期割があり

## 次世代のクラウドコンピューティング
  1. 第1の波  
      コロケーション  
      自社にデータセンターを持つ必要がない
  2. 第2の波  
      バーチャルデータセンター
  3. 第3の波  
      グローバルなエラスティッククラウド

## IaaSとPaaS
  - IaaS：Compute Engine  
      - コンピュート及びストレージ、ネットワークなどを柔軟にコントロール
  - PaaS：App Engine  
      - Java, Go, PHP, Pythonなど、焦点はアプリケーションロジック  
      - 使用した分だけの課金により、コストのオーバーヘッドを削減

## 各種サービス一例
  - コンピュート
      - Functions
      - App Engine
      - Container Engine
      - Compute Engine
  - ストレージ
      - Spanne
      - Bigtable
      - Cloud Storage
      - Cloud SQL
      - Cloud Datastore
  - ビックデータ
      - BigQuery
      - Pub/Sub
      - Dataflow
      - Dataproc
      - Datalab
  - 機械学習
      - ML Engine
      - Vision API
      - Speech API
      - Translate API
      - 自然言語 API
        
---

# モジュール2 - Google Cloud Platformのご紹介
## 概要


# モジュール3 - Google App EngineとCloud Datastore
## 概要

##ポイント
- App Engine
    - アプリケーションの稼働のために最適化
        - アプリを書くプログラマさえいれば他は不要
        - サーバー/インフラ/オペーレーターは全てGoogleが代用
        - 特にイニシャルコスト(設備/人件費)が抑えられる
- Cloud Datastore
    - リクエスト急増によるApp Engineのグレードアップ
    - グレードアップによる、DBへのリクエスト増加
        - DataStoreなら、臨機応変にDBの増強が可能
    - 落ちないアプリ作りが出来る

# モジュール4 - Google Cloud Platformストレージオプション
## 概要

## ポイント
- プロジェクトの全てのインスタンスが、共有のストレージにアクセス可能
- 別のリージョンでも、GoogleDC間の高速ネットワークによる冗長化
    - 最寄りのリージョンが落ちても、別のリージョンのバックアップでカバー
- 磁気テープは不使用(HDD/SSD)
- **オブジェクトの状態や属性に併せて自動削除**
    - アクセス頻度の高いファイル群を最前線のストレージに、低いファイル群をBigtableなどに移動など
    - 全てのファイルを同一のストレージに置く必要がないため、コスト削減に
    - 最前線のストレージがスッキリしてメンテナンス性の向上も

# モジュール5 - Google Container Engine
## 概要

# モジュール6 - Google Compute Engineとネットワーキング
## 概要

# モジュール7 ビックデータ
## 概要

# Google Cloud Platformの機械学習
## 概要

