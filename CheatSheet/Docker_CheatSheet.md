## Docker
~~~
# 基本的なDockerコマンド
Dockerイメージのビルド  : docker build -t イメージ名:タグ .
Dockerコンテナ起動      : docker run -d --name コンテナ名 イメージ名:タグ
実行中コンテナの一覧表示 : docker ps
全てのコンテナの一覧表示 : docker ps -a
コンテナ停止            : docker stop コンテナ名
コンテナ削除            : docker rm コンテナ名
イメージ一覧表示        : docker images
イメージ削除            : docker rmi イメージ名:タグ
コンテナ内でコマンド実行 : docker exec -it コンテナ名 コマンド
Dockerログ表示         : docker logs コンテナ名

~~~
