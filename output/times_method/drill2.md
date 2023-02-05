# 繰り返し処理を行うプログラムの作成

- ユーザーに数字を入力してもらい、その数の回数だけHello world!と表示させるコードを記述します。

```ruby
def output(num)
  num.times do
    puts "Hello world!"
  end
end

puts "何回表示させますか？"
num = gets.to_i
output(num)
```

