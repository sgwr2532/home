## 【シミュレーション 2】perfect shuffle
https://paiza.jp/works/mondai/b_rank_new_level_up_problems/b_rank_new_level_up_problems__perfect_shuffle
~~~
# 補足
8回ごとに元通りになる。
~~~
~~~
# コード例 (Python)
K = int(input()) %8

ls = ["S_1", "S_2", "S_3", "S_4", "S_5", "S_6", "S_7", "S_8", "S_9", "S_10", "S_11", "S_12", "S_13",
      "H_1", "H_2", "H_3", "H_4", "H_5", "H_6", "H_7", "H_8", "H_9", "H_10", "H_11", "H_12", "H_13",
      "D_1", "D_2", "D_3", "D_4", "D_5", "D_6", "D_7", "D_8", "D_9", "D_10", "D_11", "D_12", "D_13",
      "C_1", "C_2", "C_3", "C_4", "C_5", "C_6", "C_7", "C_8", "C_9", "C_10", "C_11", "C_12", "C_13"
     ]

for _ in range(K):
    half = len(ls) //2
    shuffled_ls = []
    for i in range(half):
        shuffled_ls.append(ls[i])
        shuffled_ls.append(ls[half +i])
    ls = shuffled_ls

for x in ls:
    print(x)

~~~
