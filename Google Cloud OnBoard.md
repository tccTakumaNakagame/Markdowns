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

# モジュール2 - Google Cloud Platformの入門
## 概要
- プロジェクト
- パーミッション
- IAM
- Organization
- サービスアカウント
- GCPのインターフェイス

## プロジェクト 
GCPでのプロジェクトとは、以下に関連付けられている。
- リソース等の割当
- 課金
- パーミッション
- サービスとAPI

更に、プロジェクトには3つの属性を持つ。
- プロジェクト名：重複化
- プロジェクト番号：内部で自動割当
- プロジェクトID：GPD全体でユニークなID

#＃ パーミッション
プロジェクトの中には、下記のようなメンバーが存在する。  
- オーナー  
メンバーの招待、削除、編集権限などに加え、プロジェクトの削除が可能
- 編集者(エディタ)  
アプリケーションのデプロイ、変更、ビューアの権限を含むサービスの設定
- 閲覧者  
閲覧のみ
- 課金管理者  
課金の管理、管理者の追加、削除  
社内で、運営層と課金層を分けることが可能

※複数のオーナー、編集者、閲覧者、課金管理者が存在してOK  

## IAM
IAMとは「**誰が、何を出来るか、その時どのリソースを使うか**」を定義するもの  
以下のメンバーに対して定義可能
- Googleアカウント
- サービスアカウント
- Googleグループ
- Gsuiteドメイン

また、定義されたポリシーは、組織＞プロジェクト＞リソースの順に設定可能。  
下位のポリシーは、自身そのもののポリシーと、上位のポリシーが継承され、より厳しいポリシーで上書きされる。

## Organization
Organizationは、Google Cloudリソースのルートに位置する。  
Organizationの役割は、次の2つ
- 組織管理：全てのクラウドリソースの管理
- プロジェクト作成者：プロジェクト作成の管理

## GCPのインターフェイス
GCPには、ユーザーがGCPを利用するためのインターフェイスとして、次が存在する。
- Cloud Console - Web
- Cloud SDK/ Cloud Shell
- REST-based API

### Cloud Console - Web
プロジェクトに関する全ての操作を行える
リソースの管理の他に…
- デベロッパーツール
  - Cloud Source Repositories
  - Cloud Shell
- product APIへアクセス
- プロジェクトの管理

### Cloud SDK/ Cloud Shell
GCP製品やサービス向けのCLI Toolが含まれる
- gcloud, gsutil(Cloud Storage), bq(BigQuery)

CloudShellでは、Cloud Console上で、CLIセッションを利用することが可能。  
その場で、SDK toolを利用することが出来る

### REST-base API
プログラム上から、GCPへアクセスするためのAPI
- JSON
- OAuth2.0認証

多くは、日々の割当と制限が存在するが、リクエストにより引き上げることが可能  
※必要な容量を事前に計画しておくことが重要

# モジュール3 - Google App EngineとCloud Datastore
## 概要
- Google App Engine
- Google Cloud Datastore

## Google App Engine
スケーラブルなウェブアプリや、モバイルバックエンドを構築するためのプラットフォーム(PaaS)  
App Engineが環境に関することを全て請け負い、ユーザーはアプリケーションの開発に専念することが可能

> アプリケーションの稼働のために最適化
>  - アプリを書くプログラマさえいれば他は不要
>  - サーバー/インフラ/オペーレーターは全てGoogleが代用
>  - 特にイニシャルコスト(設備/人件費)が抑えられる

Google App Engineには2つのEditionがある
- Google App Engine Standard Environment  
- Google App Engine Flexble Exvironment  

### Google App Engine Standard Environment  
- Java, PHP Goの特定のバージョン向けに管理されたランタイム
- アプリケーションの需要に合わせてインスタンスをオートスケール
- 日々の使用量に応じた料金体系
- 開発、テスト、デプロイ用SDK

### Google App Engine Flexble Exvironment  
- クリック1つでアプリの構築、デプロイ、コンテナ化
- 標準のランタイム(Python, Java, Go Node.js)でサンドボックスの制限なし(最新から、以前のバージョンまで)
- カスタムランタイムは、HTTPリクエストをサポートしていればどの言語でもOK

## Google Cloud Datastore
アプリケーションの、バックエンド向けに設計されたデータベースであり、オートスケール可能。
- NoSQL
- オートスケーリングで管理
- スキーマレスなアクセスで、構造を考慮しなくてOK
- 冗長性をビルトイン

リクエスト急増によって、App Engineがアップスケーリングがされた際にも、併せてアップスケーリングされる。  
その為、リアルタイムで急増するリクエストに対応が可能。

結果、**落ちないアプリ作り**が出来る

# モジュール4 - Google Cloud Platformストレージオプション
## 概要
- Google Cloud Storage
- Google Cloud Bigtable
- Google CLoud SQL

## Google CLoud Storage
- 管理が容易で容量のマネジメントが不要
- データは稼働中も休止中も常に暗号化される
- 全て同一のAPIでアクセス可能

### Cloud Storageのクラス
- Multi REegional  
地理的冗長性を持つ。(別のリージョンをまたがって冗長性を確保)
- Regional  
1つのリージョン内では最高レベルの環境。機械学習やワークロードに理想的
- Nearline  
データのアクセス頻度が1月あたり1回未満の用途向け
- Coldline  
データのアクセス頻度が1年あたり1回未満の用途向け

### Object Lifecycle Management
Cloud Storageの特徴の一つ  
データのバージョニングや、古くなったデータの自動削除、別のクラスへの自動移動を行う
**オブジェクトの状態や属性に併せて自動削除**
- アクセス頻度の高いファイル群を最前線のストレージに、低いファイル群をColdlineなどに移動など
- 全てのファイルを同一のストレージに置く必要がないため、コスト削減に
- 最前線のストレージがスッキリしてメンテナンス性の向上も

## Google CLoud Bigtable
テラバイトからペタバイトといった、非常に大きなデータを扱うことの出来る、フルマネージドNoSQL
- HBasse APIを使ってアクセス
- ビッグデータ、Hadoopのエコシステムとネイティブ互換を持つ
- 重複ストレージ
- もちろん、稼働中も休止中も暗号化
- Google AnalyticsやGmailなどの主要アプリケーションでも稼働

各種アプリケーションから得たビッグデータを、Bigtableに集約し、バッチ処理をする。などとが可能

## Google Cloud SQL
- クラウド上のRDB
  - MySQL
  - PostgreSQL
- 従量課金モデル
- 手頃な料金と性能
- 垂直スケーリング

## ポイント
- プロジェクトの全てのインスタンスが、共通のストレージにアクセス可能
- 別のリージョンでも、GoogleDC間の高速ネットワークによる冗長化
    - 最寄りのリージョンが落ちても、別のリージョンのバックアップでカバー
- 磁気テープは不使用(HDD/SSD)

# モジュール5 - Google Container Engine
## 概要
- Kubernetesのマネージドサービス環境
- GUI/CUI操作、APIリクエストなどにより、クラスタ環境を自動構築
- Cloud SQL、Cloud Datastoreなどと連携可能
- Serviceによるネットワーク管理と、Cloud Load Balancingのグローバルロードバランサを自動連携

# モジュール6 - Google Compute Engineとネットワーキング
## 概要
- Google Compute Engine
- Google Cloud ネットワーキング
- 運用とツール

## Google Compute Engine
App Engineでは実現できない、仮想マシン上での様々なワークロードを実行可能な環境  

ロバストなネットワーク機能
- カスタムネットワークにデフォルトで対応
- ファイアウォール
- リージョンごとのHTTPSロードバランシング
- ネットワークのロードバランシング
- サブネットワーク

CPUのコア数やメモリ量といったリソースをカスタム可能。  
また、ディスクのリサイズをダウンタイム無しで実行。自動スケーリング。  

## Google Cloud ネットワーキング
- Cloud Interconnect
- Cloud VPN
- Cloud DNS
- ロードバランシング
- Cloud CDN

### ロードバランシング
HTTPSロードバランシング
- 複数のリージョンにまたがるHTTPベースのトラフィックをバランス  
ユーザーに最も近い、最もリソースの空いたリージョンへ
- スケーラブル、暖機運転無しでレジリエンスとフォールトトレランスを提供

TCP/SSlとUDPロードバランシング
- リージョン内で、インスタンスプールに拡散
- 健全なインスタンスのみがトラフィックを維持するように保証
- スケーラブルで暖機運転不要

## 運用とツール
- Google Stackdriver
- Google Cloud Deployment manager

### Google Stackdriver
- 統合モニタリング、ロギング、診断
- GCPとAWSをまたがったワーク
- 強力なデータアナリティクスツール

主な機能
- モニタリング
- トレース
- ロギング
- エラーレポート
- デバッガ

### Google Cloud Deployment manager
- インフラストラクチャマネジメントサービス
- 繰り返し可能なデプロイを提供
