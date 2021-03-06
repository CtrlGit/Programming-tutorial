##変数
変数と聞いて数学好きの(省略)。変数は値を保存しておく箱のようなものだ。てか箱だ。正直それ以外の説明が思いつかない。のでそれで納得して欲しい

##変数を使ってみよう
変数を使ったプログラムを書いてみよう。こんな感じだ
```c
#include <stdio.h>
void main(void){
  int hako;
  int box;

  hako=1;
  box=2;
  printf("hako:%d box%d\n",hako,box);

}
```
これを実行すると
>hako:1 box:2

と画面に表示される。

##解説
3行目と4行目は変数を宣言している。最初の`int`は変数の型を表している。型とはつまり用意する箱の形を決定することだ。残念ながらコンピュータにはなんでも入れられる便利な箱は用意できないので、整数だったり文字だったりを入れる専用の箱を用意しなければいけない。intは整数を入れる箱のことだ。

型の後には変数の名前が来る。この場合hakoとboxという名前の整数を入れる箱が作られる。

6行目と7行目は変数に値を代入している。`=`は代入演算子だ。変数に値を突っ込む。なのでhakoには1が入って、boxには2が入る。

printf関数は圧倒的強さを誇る関数なので変数の中身も画面に表示できる。

始めの引数の中にある`%d`は出力変換指定子と呼ばれるもので、2つ目以降の変数の中身を指定した文字列に変換して表示することを表す記号で`%d`は整数を文字列に変換することを示す。つまり%dがhakoやboxの中身に置き換わるわけだ。

引数を複数個使う場合は`,`で区切る。printf関数で変数を画面に表示したい場合は、第1引数に出力変換指定子を表示したい変数の数だけ書いて、第2引数以降に変数をそれぞれ`,`区切りで書けばいい。

変数の基本的な使い方はこんな感じだが、わざわざ変数に値を代入して数字を表示するとか遠回りすぎてクソの極みだと感じないだろうか。変数の良さが分かるのは3章と4章が終わってからだ。なので今はとりあえず、変数がどんなものか理解しておいて欲しい。

##型
変数の型は割りと種類がある。ので下にC言語のよく使う型をまとめてみた。適切な型を使わないとうまく動作しないので気をつけよう。

ただし別の言語では型推論によって型宣言を`var`とかだけで済ますことも出来るので自分が使う言語を確認しよう。

**これはC言語の型一覧です言語によって差異が生じるので注意**

| 型 | 説明 |範囲|出力変換指定子|
|:--:|:-------:|:----:|:--------------------:||
|char|文字用の型。1文字入れておける|-128 ～ 127|%c|
|int|符号付き整数型。|-2,147,483,648 ～ 2,147,483,647|%d|
|unsigned int|符号なし整数型|0 ～ 4,294,967,295 |%d|
|double|浮動小数点型|1.7E +/- 308 (15 桁)|%f|

char型の変数には1文字代入できるし、int 型には-2,147,483,648 ～ 2,147,483,647の範囲の整数を代入できる。unsigned intはマイナスが無い代わりにより大きな数字を代入できる。またdouble型はint型では扱えない小数を扱うことが出来る。

とりあえずこの辺りの変数を使って変数の中身を表示するプログラムを組んでみよう。ちなみにC言語の文字の扱いは奇々怪々なので今はcharを使わなくてもいい。

##初期化
変数を宣言すると同時に値を代入することが出来る。これを初期化と呼ぶ。
こんな感じ。
```c
#include <stdio.h>
void main(void){
  int a=0;
  int b=5;
  printf("%d %d",a,b);
}
```
これを実行すると
>0 5

と表示される。

変数を宣言したらとりあえず初期化しておこう。値の何も入っていない変数を使うと予期しない動作をする可能性があるからだ。気になるならやってみよう。

##おまけ
変数の宣言は型が同じなら一度に宣言することが出来る。

```c
#include <stdio.h>
void main(void){
  int a,b,c,d;
}
```
もちろん初期化も出来る
```c
#include <stdio.h>
void main(void){
  int a=0,b=0,c=0,d=0;
}
```
こんな感じだ。便利なので覚えておくといい。
