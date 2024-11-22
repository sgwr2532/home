## Linux
~~~
# 定番コマンド (適宜 --help 使う)
ls, cd, pwd, cp, mv, rm, less, 
cat, head, tail, touch, uname, 
df, du, top, ps, 
ping, ifconfig, 
ssh, scp,
tar, gzip, gunzip, zip, unzip, 
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
