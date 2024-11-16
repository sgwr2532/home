## Linux
~~~
# 定番コマンド (適宜 --help 使う)
ls: ディレクトリの内容を表示
cd: ディレクトリを変更
pwd: 現在のディレクトリを表示
cp: ファイルやディレクトリをコピー
mv: ファイルやディレクトリを移動または名前変更
rm: ファイルやディレクトリを削除
cat: ファイルの内容を表示
less: 大きなファイルをページ単位で表示
head: ファイルの先頭部分を表示
tail: ファイルの末尾部分を表示
touch: 新しいファイルを作成、作成日時更新
uname: システム情報を表示
df: ディスク使用量を表示
du: ディレクトリのサイズを表示
top: リアルタイムでシステムのパフォーマンスを表示
ps: 現在のプロセスを表示
ping: ネットワーク接続を確認
ifconfig: ネットワークインターフェースを設定および表示
ssh: リモートシェルに接続
scp: リモートシステム間でファイルをコピー
tar: ファイルをアーカイブ
gzip: ファイルを圧縮
gunzip: ファイルを解凍
zip: ファイルを圧縮
unzip: ファイルを解凍
mkpasswd: password生成(-l 字数 -c 小字 -C 大字 -d 数字 -s 記号) # l以外は最低字数
~~~
~~~
*** 出力の整形 
# 最初に patternA にマッチしたものだけ置換なら g 不要
sed 's/patternA/patternB/g'
# ログ等から特定カラムの抽出
awk '{
  match($0 ,/src="[^"]+"/, src);
  match($0 ,/dst="[^"]+"/, dst);
  match($0 ,/service="[^"]+"/, service);
  print $1, $2, src[0], dst[0];
}'
# byte等の総計
awk '{
  match($0 ,/dstip="[^"]+"/, dstip);
  match($0 ,/bytes="[^"]+"/, bytes);
  print dstip[0], bytes[0];
}' |
sed 's/bytes=//' |
awk '{bytes[$1]+=$2} END {for (dist in bytes) print bytes[dist], dist}' |sort -nr



~~~
