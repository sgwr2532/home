## Linux
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
  match($0 ,/dst="[^"]+"/, dst);
  match($0 ,/bytes="[^"]+"/, bytes);
  print dst[0], bytes[0];
}' 
|awk '{bytes[$1]+=$2} END {print bytes[$1],  }'

~~~
