## Linux
~~~
# ログ等から特定カラムの抽出
awk '{
  match($0 ,/src="[^"]+"/, src);
  match($0 ,/dst="[^"]+"/, dst);
  match($0 ,/service="[^"]+"/, service);
  print $1, $2, src[0], dst[0];
}'

~~~
