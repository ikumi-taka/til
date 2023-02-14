# 計算プログラムの作成

二桁以上の整数を入力すると、十の位と一の位の数字の足し算、十の位と一の位の数字の掛け算をそれぞれ行います。<br>
最後に2つの結果を足し合わせて出力するプログラムを作成します。<br>

```ruby
def addition(a, b)
  a + b
end

def multiplication(a,b)
  a * b
end

def slice_num(num)
  tens_place = (num / 10) % 10
  ones_place = num % 10
  return tens_place, ones_place
end

puts "二桁の整数を入力してください"
input = gets.to_i

X, Y = slice_num(input)
add_result = addition(X, Y)
multiple_result = multiplication(X, Y)

puts "足し算結果と掛け算結果の合計値は#{add_result + multiple_result}です"
```

## 解説
このプログラムをターミナルで実行したときに、2桁の整数の入力を求められます。<br>
それが以下の部分です。<br>
```ruby
puts "二桁の整数を入力してください"
input = gets.to_i
```

additionメソッドで、10の位と1の位を足した計算結果をadd_resultに代入。<br>
multiplicationメソッド内で、X,Yを引数として渡し、計算結果をmultiple_resultに代入。<br>

slice_numメソッドでは、10の位と1の位をそれぞれ取得し、返り値をX, Yに代入しています。<br>
