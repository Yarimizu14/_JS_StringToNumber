====="123"の場合=====
Number(value)        => 123

parseInt(value)      => 123

parseFloat           => 123

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

parseFloat           => 123

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

parseFloat           => NaN

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

parseFloat           => 10

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

parseFloat           => 10.5

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

parseFloat           => 10.5

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

parseFloat           => 123.456

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

parseFloat           => NaN

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

parseFloat           => NaN

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

=====""の場合=====
Number(value)        => 0

parseInt(value)      => NaN

parseFloat           => NaN

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

====="Infinity"の場合=====
Number(value)        => Infinity

parseInt(value)      => NaN

parseFloat           => Infinity

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
