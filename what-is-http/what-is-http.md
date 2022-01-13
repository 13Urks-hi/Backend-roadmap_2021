# HTTPとは？

- HTTPとはホームページの閲覧に使用される[プロトコル](https://github.com/13Urks-hi/Backend-roadmap_2021/blob/main/How-does-the-internet-work/How-does-the-internet-work.md#%E3%83%97%E3%83%AD%E3%83%88%E3%82%B3%E3%83%AB)　　
  - ホームページのファイルの受け渡しは通信であり、手順・規則が必要
- WebサーバとWebブラウザで情報をやり取りし、常にやりとりは1つの要求に1つの応答の１対１
- HTTPは `HyperText Transfer Protocol` の略 

## HTTPとHTTPS

HTTPのやりとりでは、通信の内容は暗号化されていないため、盗み見ることができてしまう。  
そのため内容が暗号化されていて、内容が盗みみられてもわかりにくくなっているのが `HTTPS`

- HTTPSもHTTPと同じプロトコルの一つ
 - HTTPSはHTTPにSSL/TSLという暗号化の通信機能が付随したものがHTTPS 
- HTTPSは `HyperText Transfer Protocol　Secure` の略
