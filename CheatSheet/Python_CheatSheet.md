## Python
#### 頻出モジュール関数等
~~~
# 使い方
import モジュール(ファイル名)
 -- 実行方法: モジュール名.関数名()
from モジュール名 import 関数名
 -- 実行方法: 関数名()
numpy,decimal,
type(x), int(x), str(x), float(x), len(x), sum(x)
x.append(xx), x.remove(), x.pop(), sorted(x,reverse=True),
~~~
#### 定番表現
~~~
# 標準入出力
a = input()
a, b = input().split()
l = list(map(int, input().split()))
print(f'{x}は{y}です。')

# フォーマット
{0: <10,.3f}.format(n)  # index番号(省略可):0  ":"以降は書式  
  -- index 0番、半角スペースで左詰め最小幅10(.込み)、小数点以下3桁、型指定(fならfloat)
print("{:.{}f}".format(n, m))  # n(float型), m(小数点以下の有効桁)
print("{:i>x}".format(n))  # x 桁に右揃えで、足りない部分は i で埋める

# 改行込みでも可
print( 100 + 200 + 300
 + 400 +500 )

# 辞書  // key は一意の値
jisho ={key_0: value_0, key_1: value_1, key_2: value_2 }
print( jisho[key_0] )  # value_0 とペアの値が出力される
辞書.key()     # dict_keys型 で key全てを取得
辞書.values()  # dict_values型 で value全てを取得
辞書.items()   # key と value のペアを取得
for i, j in 辞書.items():

# 集合  // 重複しない、順序なし
x = {1,2,3,4}
x = set(リスト)
集合.add(要素)
集合.discard(要素)  # 要素がなくてもエラーにならない
集合.remove(要素)   # 要素がないとエラーになる
z = x | y    # 和集合(or)
z = x - y    # 差集合(xのみ)
z = x & y    # 積集合(共通)

# タプル  // 重複可能、順序あり
x = (1,2,3,4)
x[インデックス]

# リスト内包表記
s = [int(x) for x in list_x ]  # list_xの各要素をint型にしたリストsを作る

# 分岐
if 条件:
    処理1
elif 条件:
    処理2
else:
    処理3

# 繰り返し
for i in 繰返しオブジェクト :  # オブジェクト例 range(x),len(x),リスト等
for i in list_S :  # リストやタプルの要素を i に代入して繰り返し
for i in range(x) :
  for j in range(y) :
    # 二次元配列の全探索等。 iとj が昇順か降順か注意すること

# 関数の基本
def fanc(a, b=0):  # bのデフォルトに0
  pass  # ここで処理。"pass" とは何もしないこと
  return X  # 戻り値なければ "None" が返ってくる
fanc()
~~~
~~~
# 実践編
・flake8
エラーを無視する: # noqa: エラーコード
~~~
#### アルゴリズム等ナレッジ
~~~
~~~
