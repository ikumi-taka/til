# times文を用いてプログラムを作成する
times文を用いて、ターミナルで以下のように出力されるプログラムを作成します。
```
# ターミナル
1回目の繰り返し
2回目の繰り返し
3回目の繰り返し
4回目の繰り返し
5回目の繰り返し
6回目の繰り返し
7回目の繰り返し
8回目の繰り返し
9回目の繰り返し
10回目の繰り返し
```


模範回答
```ruby
10.times do |i|
  puts "#{i + 1}回目の繰り返し"
end
```

## 解説
```
繰り返す回数.times do |変数名|
```

times文で繰り返し処理が行われるとき、i + 1と記述しなかった場合、「0回目の繰り返し」からスタートしてしまいます。<br>
そのため、「i+ 1」と書いています。<br>
