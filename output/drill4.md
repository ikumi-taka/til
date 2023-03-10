# 条件演算子を使ってプログラムを書く
3桁の正の整数を入力します。その整数の「百の位・十の位・一の位の和」について、<br>
10の倍数（10,20,30...）からの差が<br>
- 2以内であるときは"True"
- それ以外は"10の倍数との差は○です"
と表示されるようにしましょう。<br>

```
出力例：
near_ten(117)→True
near_ten(123)→10の倍数との差は4です
near_ten(111)→10の倍数との差は3です
```
百の位・十の位・一の位の和が6などの時に、「10の倍数との差は6です」と出力せずに、「10の倍数との差は4です」と10の倍数から近い方の差を出力するようにしてください。また、0も10の倍数に含むものとします。<br>

```ruby
模範回答
def near_ten(num)
  total = (num / 100) + (num / 10 % 10) + (num % 10)
  remainder = total % 10
  if remainder <= 2 || remainder >= 8
    puts "True"
  elsif remainder <= 5
    puts "10の倍数との差は#{remainder}です"
  else
    puts "10の倍数との差は#{10 - remainder}です"
  end
end

# 呼び出し例
near_ten(300)
```

## 解説
100の位, 10の位, 1の位を足した数値をtotalにまとめました。<br>
remainderは、100の位, 10の位, 1の位を足した数値を10で割ったあまりの数値を計算。<br>
```ruby
if remainder <= 2 || remainder >= 8
```
上記コードは「remainderが10の倍数との差が2以内である場合」と意味します。

```ruby
elsif remainder <= 5
  puts "10の倍数との差は#{remainder}です"
```
elsifはremainderが5以下のとき、つまり3か4か5のときに「"10の倍数との差は#{remainder}です"」と返すよう記述しています。<br>
※５以下なので1, 2も当てはまるのでは？と最初思っていましたが、<br>
10の倍数との差が2以下の場合はTrueと返すよう指示があったので、該当しません。<br>

```ruby
else
  puts "10の倍数との差は#{remainder}です"
```
elseでは、remainderが6か7のときに「"10の倍数との差は#{10 - remainder}です"」と変えるよう記述しています。

