# 簡易的な掲示板

木曜1, 2限「システム開発」授業の実習用です。

## 以下を学習するために掲示板を作成します。
・基礎的なWebサーバーサイド技術について理解し，説明できる。
・ 一人で何もない状態からWebサービスを制作しインターネットに公開できる。

## 使い方
### 起動
本リポジトリのプロジェクトルートで、以下のコマンドを実行すると各コンテナが起動します
```sh
docker compose up
```

### テーブル作成
各コンテナが起動している状態で、以下のコマンドを叩くことにより、MySQLクライアントを起動します。
```sh
docker compose exec mysql mysql techc
```

以下のSQLを実行し、テーブルを作成します。
```sh 
CREATE TABLE `bbs_entries` (
    `id` INT UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY,
    `body` TEXT NOT NULL,
    `created_at` DATETIME DEFAULT CURRENT_TIMESTAMP,
    'image_filename' TEXT DEFAULT NULL;
);
```

### ブラウザからアクセス
以下のURLで、ブラウザから掲示板にアクセスできます。
[http://{EC2インスタンスのIPアドレス}/bbsimagetest.html](http://{EC2インスタンスのIPアドレス}/bbsimagetest.html)

## 作成者
 
作成情報を列挙する
 
* 津澤友喜
* 東京デザインテクノロジーセンター専門学校3年プログラマー専攻
* tomoki.tsuzawa@gmail.com
