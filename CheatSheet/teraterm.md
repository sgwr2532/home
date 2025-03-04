## teraterm
~~~

~~~
#### マクロのサンプル
~~~
# ログイン
;; SSH Login
connect 'ホスト:22 /ssh /auth=publickey /user=$user_name$ /keyfile=$key_path$ /passwd=$pass_phrase$'
wait '$'
;; コマンドを自動投入し、ディレクトリ移動やSSHで踏み台とする
sendln '投入コマンド'
wait '$'

# 

~~~
