# FizzBuzz応用問題

FizzBuzzという言葉遊びがあります。<br>
1から数を数えていく際に、それが3の倍数だったら「Fizz」, 5の倍数だったら「Buzz」と言う、というものです。<br>
ただし、15の倍数の時は「FizzBuzz」と言います。<br><br>

例） 1, 2, Fizz, 4, Buzz, Fizz ,,,,<br><br>

このFizzBuzzを再現できるメソッドを作成してください。<br>
ただし、いくつまでカウントするか、引数で指定できるものとします。<br>

- ヒント
範囲を指定して繰り返しをする場合は、範囲演算子(..)を使用します。<br>
以下のように使用します。
```
(開始する値..終了する値）
```
具体的には以下のように使用できます。
```ruby
# 1～6までの範囲を指定して、繰り返し表示
(1..6).each do |num|
  puts num
end
```

模範解答
```ruby
def fizzbuzz(max_num)
  (1..max_num).each do |num|
    if num % 15 == 0
      puts "FizzBuzz"
    elsif num % 3 == 0
      puts "Fizz"
    elsif num % 5 == 0
      puts "Buzz"
    else
      puts num
    end
  end
end

puts 'いくつまで数えますか？'
num = gets.to_i
fizzbuzz(num)
```
## 解説
範囲演算子「　..　」を使用して1から指定された数字（max_num）まで繰り返し処理を行います。<br>
その次に、条件分岐であるif文の条件に沿って「Fizz」「Buzz」「FizzBuzz」の処理を行います。<br>
