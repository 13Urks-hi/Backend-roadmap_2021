# ドメイン名とは？
インターネット上でWebサイトを閲覧したり、電子メールを送信したりする際に、  
その情報がインターネット上のどこにいるのかを特定するためのものいわゆるインターネット上の住所。  

- パブリックIPアドレスからアクセス可能で、IPv4では32ビット（0〜255までの４桁の数値　例>`173.194.121.32`） として記述される
- IPv6では128ビット（通常は転んで区切られた4桁の16進数の8つのグループ例> `2027:0da8:8b73:0000:0000:8a2e:0370:1337`） として記述される
- ドメイン名とは `ドメイン名` の部分(太字は**ホスト名**)
  - メールアドレスの場合: **www**.`example.co.jp`
  - Webページの場合: **Urks-hi**@`example.co.jp`

## ドメイン名の構造 🌎
ドットで区切られたいくつか（1つだけとか3つとか色々）からなっており、**右から左に向かって読まれる**

### TLD（トップレベルドメイン）
もっとも一般的な情報を提供する箇所。`.com`, `.net`, `.org` のこと。

- より厳密な基準を適用するために目的がより明確なものもある
  - `.jp` などはローカルTLD、特定の言語で提供しているか、特定の国でホスティングされていることを要求する
    - **その国のリソースだよ〜** と言うこと
  - `.gov`, `.go.jp` を含むものは、**政府機関**のみが使用可能
  - `.edu`, `.ac.jp` は**教育・学術機関**のみで使用されている
- 特殊文字も含めることができ、長さは最大63文字（でも大体は2,3文字）

### ラベル（コンポーネント）
TLDの後に続くもので、一文字から一文までなんでも良い。TLDの直前にあるラベルは、 *二次レベルドメイン* とも呼ばれる。  
- ドメイン名は多数のラベルを持つことが可能で、ドメイン名を構成するのに3つであることが必須ではない
- 制御権のあるドメインには、`developer.xx.com` と `iot.xx.com` のように互いに異なる内容で *サブドメイン* を作成することができる

## 使えるドメイン名をさがす🔍
特定のドメイン名が利用可能かどうか調べるには、ドメイン名の登録機関のサイトにアクセスし、`whois` と言うサービスを大体の機関は提供しているはずなので、それを使う。
または、シェルを内蔵しているシステムを使っている場合は、 `whois` コマンドを入力する。

- シェルを使った場合（`mozilla.org`を拝借）
  - 登録されていないドメイン名で探そうとすると `NOT FOUND` と表示される
```$ whois mozilla.org
Domain Name:MOZILLA.ORG
Domain ID: D1409563-LROR
Creation Date: 1998-01-24T05:00:00Z
Updated Date: 2013-12-08T01:16:57Z
Registry Expiry Date: 2015-01-23T05:00:00Z
Sponsoring Registrar:MarkMonitor Inc. (R37-LROR)
Sponsoring Registrar IANA ID: 292
WHOIS Server:
Referral URL:
Domain Status: clientDeleteProhibited
Domain Status: clientTransferProhibited
Domain Status: clientUpdateProhibited
Registrant ID:mmr-33684
Registrant Name:DNS Admin
Registrant Organization:Mozilla Foundation
Registrant Street: 650 Castro St Ste 300
Registrant City:Mountain View
Registrant State/Province:CA
Registrant Postal Code:94041
Registrant Country:US
Registrant Phone:+1.6509030800
```  

## ドメイン名の取得 📛
- ドメイン名は住所のようなものなので、重複して登録することは不可
   - ドメイン取得は早い者勝ち
- **レジストラ** と言う組織に申し込みを行う必要がある
  - ICANN[^1]に認定されているレジストラはレジストラの認定方針とレジストラ認定規約に基づいて、技術や能力を持っているドメイン登録業者をレジストラと言う
  - レジストラは各レジストリとレジストリ・レジストラ契約を結びSRS[^2]を使用してレジストリデータベースに直接ドメイン情報を登録する

### 流れとしては以下のような感じ
 1. 登録機関のウェブサイトにアクセス
 2. 「ドメイン名を取得する」と言う操作（クリック！）
 3. フォームに必要事項を記入して、登録したいドメイン名に間違いがないことをよ〜く確認（支払った後に気づくと遅い）
 4. 登録機関が、ドメイン名が正しく登録されたことを知らせてくれる
 
[^1]: **ICANN(The Internet Corporation for Assigned Names and Numbers)**: ドメイン名の登録業務、IPアドレスなどの管理責任を民間のインターネットの非営利団体に移管する方針で設立された団体
[^2]: **SRS(Shared Registry System)**: レジストリと米国政府が合意した同意書により、色々なレジストラがドメイン登録サービスを提供できるシステムのプロトコルと関連するソフトウェア
