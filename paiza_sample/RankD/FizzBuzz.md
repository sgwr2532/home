## FizzBuzz Python3編（paizaランク D 相当）
https://paiza.jp/works/mondai/d_rank_level_up_problems/d_rank_level_up_problems__loop_boss
~~~
1 ~ 100 の整数に対して、3 と 5 の両方で割り切れるなら FizzBuzz を、 3 でのみ割り切れるなら Fizz 、
5 でのみ割り切れるなら Buzz を改行区切りで出力してください。
また、どちらでも割り切れない場合は、その数字を改行区切りで出力してください。
~~~
~~~
# コード例
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)

~~~
