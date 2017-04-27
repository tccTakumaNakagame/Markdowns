# Fotigate初期設定

# AGENDA
1. 言語変更
2. Timezoneの設定
3. インターフェースの設定
4. VLANの設定
5. ルーティングの設定
6. ポリシーの設定
7. HA(冗長)の設定

# 
## 0. 前準備
- FortiGateの管理インターフェースとPCを接続
※なければPort1
- https://192.168.1.99にアクセス
- 以下でログイン
  - user: admin
  - pass: なし

## 1. 言語変更
`Admin -> Settings -> Language`
<http://w.builwing.info/2011/04/01/fortigate%E3%81%AE%E5%88%9D%E6%9C%9F%E8%A8%AD%E5%AE%9A/>

## 2. Timezoneの設定
`システム -> ダッシュボード -> Status`

## 3. インターフェースの設定
`システム -> ネットワーク -> インターフェース`  
<http://www.viva-fortigate.com/archives/16819499.html>

## 4. VLANの設定
`システム -> ネットワーク -> インターフェース`左上の`Create New`
<http://www.viva-fortigate.com/archives/15907019.html>

## 5. ルーティングの設定
`システム -> ネットワーク -> Routing`左上の`新規作成`  
<http://network-beginner.xyz/fortigate-static-route>

## 6. ポリシーの設定
`Policy & Objects -> Policy -> IPv4`  
<http://www.viva-fortigate.com/archives/cat_660091.html>

## 7. HA(冗長)の設定
`設定 -> HA`  
http://www.viva-fortigate.com/archives/15906866.html

## そのほか
[CLI基本コマンド](http://www.viva-fortigate.com/archives/16377634.html)

### Procurve初期設定
#### 基本設定
<http://qiita.com/ressei3rd/items/c6b2a8ebea7a700504a9>

#### タイムゾーンが正しく反映されない場合
<http://dynamic-one.com/archives/51536282.html>
