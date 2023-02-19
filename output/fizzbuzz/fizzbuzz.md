# FizzBuzz問題
この問題は非常に有名なプログラミングの問題だそうです。<br>
1〜100までの数字をターミナルに出力します。<br>
ただし、「3の倍数」のときは数字の代わりに文字列でFizzと、「5の倍数」のときはBuzz、両方の倍数である「15の倍数」のときはFizzBuzzと出力するようにします。<br>

## 条件
- 値が15の倍数である
- 値が3の倍数である
- 値が5の倍数である
- 上の3つの条件のどれにもあてはまらない
- 「〇〇の倍数」を導き出す時は剰余演算子を用いる
- 条件を指定して繰り返し処理をする場合は、whileというメソッドを使う

模範解答
```ruby
def fizz_buzz
  num = 1
  while (num <= 100) do
    if (num % 3 == 0) && (num % 5 == 0)
      puts "FizzBuzz"
    elsif (num % 3) == 0
      puts "Fizz"
    elsif (num % 5) == 0
      puts "Buzz"
    else
      puts num
    end

    num = num + 1
  end
end

fizz_buzz
```
ターミナル出力
```ruby
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz
Fizz
22
23
Fizz
Buzz
26
Fizz
28
29
FizzBuzz
31
32
Fizz
34
Buzz
Fizz
37
38
Fizz
Buzz
41
Fizz
43
44
FizzBuzz
46
47
Fizz
49
Buzz
Fizz
52
53
Fizz
Buzz
56
Fizz
58
59
FizzBuzz
61
62
Fizz
64
Buzz
Fizz
67
68
Fizz
Buzz
71
Fizz
73
74
FizzBuzz
76
77
Fizz
79
Buzz
Fizz
82
83
Fizz
Buzz
86
Fizz
88
89
FizzBuzz
91
92
Fizz
94
Buzz
Fizz
97
98
Fizz
Buzz
```

## 解説
1〜100までの数字をターミナルに出力するためのコードを記述します。
```ruby
def fizz_buzz
    num = 1
    while (num <= 100) do
      puts num

      num = num + 1
    end
  end

  fizz_buzz
```
次に、条件分岐内で15の倍数、3の倍数、5の倍数のときに、それぞれどのワードを出力させるのか、書く順番に注意をしてコードを記述します。

```ruby
if (num % 3 == 0) && (num % 5 == 0)
```
この部分は、15の倍数のときの条件を表していますが、
```ruby
if (num % 15 == 0)
```
上記のように書いても良いですね。
