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

## 解説

- メソッド外の部分
```ruby
puts "何回表示させますか？"
num = gets.to_i
output(num)
```
上記コードは、ファイルを実行したときにターミナルで出力される内容を書いています。<br>
ユーザーに数字を入力させることで、「Hello world!」が何回表示されるのかを実行するためです。<br>
getsメソッドで入力した値は、全て文字列で返します。<br>
そのため、***.to_i***を付けて数値に変換させます。<br><br>

- output(num)<br>
ユーザーが入力した数値を、メソッド内で呼び出したいため、numという引数を使います。<br>

- outputメソッド内<br>
繰り返し表示させるためには、timesメソッドを使います。<br>
ユーザーがターミナルで入力した数値が変数numに代入され、処理が行われるということです。<br>



