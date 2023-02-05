# eachメソッドについて

eachメソッドは、配列や要素の１つひとつに対して、要素の数だけ名前をつけて取り出すことができる処理を行います。

例
```ruby
colors = ["赤", "黄", "青"]

colors.each do |color|
  puts "#{color}色"
end
```

```ruby
赤色
黄色
青色
# ターミナル出力
```
each doの後にブロック変数（　|[変数]|　）を記述します。<br>
そうすることで、繰り返し処理が実行されるたびに、配列・ハッシュの値がそれぞれブロック変数に格納され、その値を処理の中で使用することができます。<br>


# timesメソッドで配列の全ての要素に対して繰り返し処理を書くとどうなる？
例
```ruby
colors = ["あか", "あお", "きいろ"]
element_count = colors.length  # 要素数を変数に代入

element_count.times do |i|
   puts "色: #{colors[i]}"  # 添字0から要素を出力
end
```

```ruby
色: あか
色: あお
色: きいろ
```

ぱっと見、コードが長く読みにくいように感じます。<br>
そのため、配列やハッシュの要素を全て取り出すときは、eachメソッドを使います。<br>