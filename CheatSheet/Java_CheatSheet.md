## Java
~~~
# Javaの使い方
> javac xxxx.java
> java クラス名
※ main()メソッドを含むクラスじゃないとエラーになる
 + ソースファイルモードで実行
> java xxxx.java
~~~
~~~
# コード例
import java.util.*;
public class Main {
    public static void main(String args) {
        Scanner sc = new Scanner(System.in);
        List<Integer> list_a = new ArrayList<>();
        String ans = sc.nextLine();
        System.out.println("XXXXXX");
        System.out.println(list_a);
        System.out.println(ans);
        for (int x : list_a) {
            System.out.println(x);
        }
    }
}
~~~
