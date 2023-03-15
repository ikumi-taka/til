# 引数を使ってプログラムを作ろう
< 問題 ><br>
ユーザーが数字を2つ渡すと、それらを掛け算した結果を返すプログラムを作ってください。<br>
2つの数字を、それぞれnum1, num2という変数にgetsメソッドを利用して定義してください。<br>

```ruby
# 自分の回答
def two_nums(num1, num2)
  result = num1 * num2
  puts "#{num1}と#{num2}をかけた答えは#{result}です"
end


puts "最初の数字を入力してください"
num1 = gets.to_i
puts "2番目の数字を入力してください"
num2 = gets.to_i

two_nums(num1, num2)
```

```ruby
# 模範回答
def multiplication(num1, num2)
  puts "#{num1}と#{num2}をかけた答えは#{num1 * num2}です！"
end

puts "最初の数字を入力してください"

num1 = gets.to_i

puts "2番目の数字を入力してください"

num2 = gets.to_i

multiplication(num1, num2)
```

## 解説
メソッドには複数の引数を渡すことができます。<br>
複数の引数を渡した場合、引数を受け取る方は、メソッドの呼び出し順で引数を順番に代入されます。<br>
