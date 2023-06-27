【Javaとは】

Javaは世界中にたくさんの開発者がいる有名な言語。
大規模システム、Webアプリケーション、スマートフォンアプリなど様々な場所で活躍している言語。
(JavaとJavaScriptは無関係)

●Javaを動かしてみる
　　VSコードにてMain.javaファイルを作成して
 System.out.println("Hello World");
 を入力すると、コンソールにて
 Hello World が出力される。
 
●出力の命令
 System.out.println()は、()の中身を出力(表示)せよという命令。
 
●Javaの構造
 class Main { 　                                  クラス部分
  public static void main(Staring[] args) {      メソッド部分
  //ここにコードを書く　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　処理部分
  }
 }
 
●Javaは文の終わりに必ずセミコロン(;)を付けること。
●コード内にコメントを書くことができる。
 //と書くことでそこから行末までがコメントアウトされる。

●数値
　　数値は文字列と違い、ダブルクォーテーションで囲わない。
 足し算や引き算も可能。
　　記号の前後に半角スペースを入れるを見やすい。
  
 コード　　System.out.println(3);
      　System.out.println(5 + 2); 　足し算
      　System.out.println(8 - 5);　　　引き算
      　System.out.println(3 * 2);　　　掛け算
      System.out.println(6 / 2);　　　　割り算
      System.out.println(8 % 5);　　　　１余り３
       
 コンソール　　3  7  3 　6　　　３　とそれぞれ出力される

●データ型
　　文字列や数値という値の種類はデータ型と呼ばれる。
 "Hello World"　(文字列)... String型　(Sは大文字)
 ３　（整数）... int型　(iは小文字、integerを意味する)

●変数
　　変数とはデータを入れる箱のようなもの。
 変数には名前(変数名)がついており、いつでも値が取り出すことができる。
 
●変数の定義
　　まず変数を"定義"する必要がある。
 ①変数に入れる値のデータ型を指定する
 ②変数の名前を決める
 
 String型の変数定義
 ①String ②name; ....①データ型、②変数名
 int型の変数定義
 ①int ②number; ....①データ型、②変数名
 
●値の代入
　　変数を定義したら値を入れる。このことを代入と呼ぶ。「変数名＝値」とするだけで代入できる。
 int number;
 number = 3; ....numberに3を代入
 
 String name;
 name = "Sato" ....Stringに"Sato"を代入
 
●変数から値を取り出す
　　int number;
 number = 10;
 System.out.println(number); .....コンソールで１０と表示される
 
 String name;
 name = "Sato"
 System.out.println(name); .....コンソールでSatoと表示される
 
●変数の初期化
　　int number = 3;
 String text = "Hello World";
  ※変数の定義と同時に値を代入　(=変数の初期化)
  
●int型変数の計算
　　int number1 = 10;
 System.out.println(number1 + 3); ....... コンソールで１３が出力
 
 int number2 = 5;
 System.out.println(number1 + number2); ......コンソールで１５が出力
 
●String型変数の連結
　　String greeting = "こんにちは";
 System.out.println(greeting + "佐藤さん")
 
 String name = "鈴木さん";
 System.out.println(greeting + name);  (変数名には""をつけない)
 ↓
 コンソールで　　　　　こんにちは佐藤さん
 　　　　　　　　　　　　　　　　　　　　　　　こんにちは鈴木さん　　　　　が出力される

●変数の更新時の注意点
　　int number = 3;
 number = 5;   ......値を更新する時はデータ(int)型を付けない。                      
                      
●自己代入
　　int X = 3;
 System.out.println(X);  ......コンソールで３の表示
 X = X + 2;
　　System.out.println(X);  ......コンソールで５の表示
  
●自己代入の省略した書き方
　　X = X + 10; ...... X += 10;
 X = X - 10; ...... X -= 10;
 X = X * 10; ...... X *= 10;
 X = X / 10; ...... X /= 10;
 X = X % 10; ...... X %= 10;
 
●１を足す、１を引く
　　X = X + 1; ---➔ X += 1; ---➔ X++;　　　　１を足すという意味になる
 X = X - 1; ---➔ X -= 1; ---➔ X--;　　　　１を引くという意味になる
 
●なぜ変数を使うのか
　　①何のデータか分かりやすい
　　②pな時データを繰り返し使える
　　③変更に対応しやすい
  
●変数の役割
　　String text = "こんにちは"；
 System.out.println("A　さん" + text);
 System.out.println("B　さん" + text);
 System.out.println("C　さん" + text);　　　　　　としておいた方が便利で修正も楽
 
●変数の注意点
　　良い例　　　　date .....英単語を用いる
  　　　　　　　　　　　　userName ......２種類以上の場合は大文字で区切る(キャメルケース)
 悪い例　　　　1name ......　✖　数字開始
 　　　　　　　　　　　　　　first_name ..... ▲　アンダーバー　（スネークケース）
        namae ...... ▲　ローマ字
　　　　　　　　　　　　　　　　名前　....... ▲　日本語

●小数を扱う　（double型）
　　５.....int型　（整数）
 ３．１４.....double型　(小数)
 
●型変数について　
　　　System.out.println("佐藤さんは" + 23 + "歳です");　➔　佐藤さんは２３歳です　　
