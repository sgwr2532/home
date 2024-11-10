## Python
#### 頻出モジュール関数等
~~~
numpy,decimal,
type(x), int(x), str(x), float(x), len(x),
x.append(xx), x.remove(), x.pop(), sorted(x,reverse=True),
~~~
#### 定番表現
~~~
# 標準入出力
a = input()
a, b = input().split()
l = list(map(int, input().split()))
print(f'私は{x}です。')

# n(float型), m(有効桁)
print("{:.{}f}".format(n, m))

# 改行込みでも可
print( 100 + 200 + 300
 + 400 +500 )

# 辞書
jisho ={key_0: value_0, key_1: value_1, key_2: value_2 }
print( jisho[key_0] )  # value_0 の値が出力される

# リスト内包表記
s = [int(x) for x in list_x ]

# 分岐
if 条件:
    処理1
elif 条件:
    処理2
else:
    処理3

# 繰り返し
for i in range(x):
for i in len(xxx):
for i in list:  # 

~~~

