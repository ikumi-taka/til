# eachの入れ子

```ruby
fruits_price = [["apple", [200, 250, 220]], ["orange", [100, 120, 80]], ["melon", [1200, 1500]]]
```
上記配列を利用して、apple, orange, melonそれぞれの合計金額を出力するプログラムを書きます。<br>

```ruby
fruits_price = [["apple", [200, 250, 220]], ["orange", [100, 120, 80]], ["melon", [1200, 1500]]]

fruits_price.each do |fruit|
  sum = 0
  fruit[1].each do |price|
    sum += price
  end
  puts "#{fruit[0]}の合計金額は#{sum}円です"
end
```

- fruits_price.each do |fruit|<br>
["apple", [200, 250, 220]という値を取り出し、変数fruitに代入します。<br>
- その次の行〜endまではfruitの値をいつずつ取り出して、自己代入をしながらsumを出力します。<br>
詳細に見ると以下の通りです。<br>

```ruby
# 1回目
sum = 0
#sum += priceはsum = sum + priceと解釈できる
sum = 0 + 200
# 返り値
sum = 200

#2回目 
#sumは1回目の200という値が返されます
sum = 200
sum = 200+ 250
sum = 450

#3回目 
#sumは2回目の450という値が返されます
sum = 450
sum = 450+ 220
sum = 670
```

というのを、残りのorangeとmelonでも同じように繰り返し処理をします。<br>
ターミナルでは以下のように出力されます。

```
appleの合計金額は670円です
orangeの合計金額は300円です
melonの合計金額は2700円です
```
