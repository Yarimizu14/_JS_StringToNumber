##文字列＝＞数値
文字列から数字を取り出す方法について調べてみた。

方法として

* Numberを使う方法
* parseInt, parseFloatを使う方法
* 一旦演算をする方法
* ビット演算子を使う方法

の４つの方法があるらしい。

結果として

* parseInt, parseFloatは数値の後に文字列が混じっていても数値だけ取り出せる。
* 演算して取得する方法は、小数の場合も取り出してくれる。取り出せない場合は、NaNやInfinityを返す。
* ビット演算子は、小数は取り出せず、取り出せない場合は０を返すことが多い。
* Booleanを渡した場合、trueの時１、falseの時に０を返すものが多い。

n = (文字列ー＞数値変換)をした場合、

if(n)で意図せず弾けないの場合がありそうなのは、trueで１が返ってくる場合とかInfinityの場合など。

あとは、'100px'、'100m'など単位付きの文字列をどう扱うかで、使うべき変換の仕方が変わりそう。

====="123"の場合=====

Number(value)        => 123

parseInt(value)      => 123

parseFloat(value)    => 123

+value               => 123

value - 0            => 123

value * 1            => 123

value / 1            => 123

-(-value)            => 123

~~value              => 123

value&-1             => 123

value|0              => 123

value^0              => 123

value>>0             => 123

value<<0             => 123

====="123hoge"の場合=====

Number(value)        => NaN

parseInt(value)      => 123

parseFloat(value)    => 123

+value               => NaN

value - 0            => NaN

value * 1            => NaN

value / 1            => NaN

-(-value)            => NaN

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="hoge123"の場合=====

Number(value)        => NaN

parseInt(value)      => NaN

parseFloat(value)    => NaN

+value               => NaN

value - 0            => NaN

value * 1            => NaN

value / 1            => NaN

-(-value)            => NaN

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="010"の場合=====

Number(value)        => 10

parseInt(value)      => 10

parseFloat(value)    => 10

+value               => 10

value - 0            => 10

value * 1            => 10

value / 1            => 10

-(-value)            => 10

~~value              => 10

value&-1             => 10

value|0              => 10

value^0              => 10

value>>0             => 10

value<<0             => 10

====="010.50"の場合=====

Number(value)        => 10.5

parseInt(value)      => 10

parseFloat(value)    => 10.5

+value               => 10.5

value - 0            => 10.5

value * 1            => 10.5

value / 1            => 10.5

-(-value)            => 10.5

~~value              => 10

value&-1             => 10

value|0              => 10

value^0              => 10

value>>0             => 10

value<<0             => 10

====="010.50hoge"の場合=====

Number(value)        => NaN

parseInt(value)      => 10

parseFloat(value)    => 10.5

+value               => NaN

value - 0            => NaN

value * 1            => NaN

value / 1            => NaN

-(-value)            => NaN

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="123.456hoge"の場合=====

Number(value)        => NaN

parseInt(value)      => 123

parseFloat(value)    => 123.456

+value               => NaN

value - 0            => NaN

value * 1            => NaN

value / 1            => NaN

-(-value)            => NaN

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="true"の場合=====

Number(value)        => 1

parseInt(value)      => NaN

parseFloat(value)    => NaN

+value               => 1

value - 0            => 1

value * 1            => 1

value / 1            => 1

-(-value)            => 1

~~value              => 1

value&-1             => 1

value|0              => 1

value^0              => 1

value>>0             => 1

value<<0             => 1

====="false"の場合=====

Number(value)        => 0

parseInt(value)      => NaN

parseFloat(value)    => NaN

+value               => 0

value - 0            => 0

value * 1            => 0

value / 1            => 0

-(-value)            => 0

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

=====""（空文字）の場合=====

Number(value)        => 0

parseInt(value)      => NaN

parseFloat(value)    => NaN

+value               => 0

value - 0            => 0

value * 1            => 0

value / 1            => 0

-(-value)            => 0

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="-10"の場合=====

Number(value)        => -10

parseInt(value)      => -10

parseFloat(value)    => -10

+value               => -10

value - 0            => -10

value * 1            => -10

value / 1            => -10

-(-value)            => -10

~~value              => -10

value&-1             => -10

value|0              => -10

value^0              => -10

value>>0             => -10

value<<0             => -10

====="-10.5"の場合=====

Number(value)        => -10.5

parseInt(value)      => -10

parseFloat(value)    => -10.5

+value               => -10.5

value - 0            => -10.5

value * 1            => -10.5

value / 1            => -10.5

-(-value)            => -10.5

~~value              => -10

value&-1             => -10

value|0              => -10

value^0              => -10

value>>0             => -10

value<<0             => -10

====="-10.5hoge"の場合=====

Number(value)        => NaN

parseInt(value)      => -10

parseFloat(value)    => -10.5

+value               => NaN

value - 0            => NaN

value * 1            => NaN

value / 1            => NaN

-(-value)            => NaN

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="-10hoe.5"の場合=====

Number(value)        => NaN

parseInt(value)      => -10

parseFloat(value)    => -10

+value               => NaN

value - 0            => NaN

value * 1            => NaN

value / 1            => NaN

-(-value)            => NaN

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="-hoge10"の場合=====

Number(value)        => NaN

parseInt(value)      => NaN

parseFloat(value)    => NaN

+value               => NaN

value - 0            => NaN

value * 1            => NaN

value / 1            => NaN

-(-value)            => NaN

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0

====="Infinity"の場合=====

Number(value)        => Infinity

parseInt(value)      => NaN

parseFloat(value)    => Infinity

+value               => Infinity

value - 0            => Infinity

value * 1            => Infinity

value / 1            => Infinity

-(-value)            => Infinity

~~value              => 0

value&-1             => 0

value|0              => 0

value^0              => 0

value>>0             => 0

value<<0             => 0
