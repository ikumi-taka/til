# if, else問題

条件分岐を利用して、プログラムを作成していきます。<br>
内容は下記の通りです。<br>
ECサイトのポイント付与サービスを考えます。<br>
購入金額が999円以下の場合、3%のポイント<br>
購入金額が1000円以上の場合、5%のポイント<br>
このように付与されるポイントを出力するメソッドを作りましょう。<br><br>

ただし誕生日の場合はポイントが5倍になります。<br>
誕生日の場合はtrue, 誕生日でない場合はfalseで表します。<br>
また、小数点以下をすべてのポイント計算が終わったあとに切り捨てましょう。<br>


```ruby
def calculate_points(amount, is_birthday)
  if amount <= 999
    point = amount * 0.03
  else
    point = amount * 0.05
  end
  if is_birthday
    point = point * 5
  end
  puts "ポイントは#{point.floor}点です"
end

# 呼び出し例
calculate_points(500, false)
calculate_points(2000, false)
calculate_points(3000, true)
```


ターミナルには以下のように出力されます。

```ruby
ポイントは15点です
ポイントは100点です
ポイントは750点です
```


## 解説
ポイント
- 購入金額によってポイント付与の割合が異なること
- 誕生月は購入金額とは別でif文を使ってコードを書くこと

また、付与するポイントの計算結果については、小数点以下は切り捨てするという条件が提示されているため.floorメソッドを使って切り捨てます。
