## PostgreSQL
~~~
# 導入
sudo apt-get install curl ca-certificates gnupg
curl https://www.postgresql.org/media/keys/ACCC4CF8.asc | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/apt.postgresql.org.gpg >/dev/null
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
sudo apt-get update
sudo apt-get install postgresql
sudo systemctl status postgresql
sudo systemctl start postgresql
sudo systemctl enable postgresql
sudo passwd postgres
接続: psql データベース名(省略可)

# ユーザーの操作
ユーザーの作成: CREATE USER ユーザー名 WITH PASSWORD 'パスワード';
ユーザーの削除: DROP USER ユーザー名;
ユーザーの一覧表示: \du

# データベースの操作
データベースの作成: CREATE DATABASE データベース名;
データベースの削除: DROP DATABASE データベース名;
データベースの一覧表示: \l   # DB外、OS側では psql-l
データベースのバックアップ: pg_dump データベース名 > バックアップファイル名.sql
データベースのリストア: psql データベース名 < バックアップファイル名.sql

# テーブルの操作
テーブルの作成: CREATE TABLE テーブル名 (カラム名 データ型, カラム名 データ型);
テーブルの削除: DROP TABLE テーブル名;
テーブルの一覧表示: \dt
テーブルの構造確認: \d テーブル名
テーブルのリネーム: ALTER TABLE 古いテーブル名 RENAME TO 新しいテーブル名;
カラムの追加: ALTER TABLE テーブル名 ADD COLUMN カラム名 データ型;
カラムの削除: ALTER TABLE テーブル名 DROP COLUMN カラム名;

# データの操作
データの挿入: INSERT INTO テーブル名 (カラム名, ...) VALUES (値, ...), (値, ...);
データの更新: UPDATE テーブル名 SET カラム名 = 新しい値 WHERE 条件;
データの削除: DELETE FROM テーブル名 WHERE 条件;
データの選択: SELECT カラム名 FROM テーブル名 WHERE 条件;
データの一括挿入: COPY テーブル名 (カラム名, ...) FROM 'ファイルパス' DELIMITER ',' CSV HEADER;
データの一括エクスポート: COPY (SELECT * FROM テーブル名) TO 'ファイルパス' DELIMITER ',' CSV HEADER;

# その他の便利なコマンド
データベースへの接続: \c データベース名
SQLファイルの実行: \i ファイルパス
ヘルプの表示: \?
~~~
