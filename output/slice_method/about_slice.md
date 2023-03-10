# slice!メソッド
配列や文字列から指定した要素を削除し、削除したあとの要素を返します。<br>
「　!　」の付くメソッドは***破壊的メソッド***と言います。<br>

## 破壊的メソッド
元の配列や文字列そのものを変化させてしまうメソッドのことを破壊的メソッドと言います。<br>

ちなみに、調べてみると「　!　」が付かない破壊的メソッドもあります。<br>
勉強する必要がありますね！<br>


## slice!メソッドの例

```ruby
string = "おはようございます！"
string.slice!(2)

puts string
#=> "おはうございます！"
# 2番目の要素の「　よ　」が取り除かれて、返ってきた
```

# sliceメソッド
上記は「　！　」がついた破壊的メソッドでした。<br>
ここでは、sliceメソッドについて説明します。<br>
配列や文字列から、指定した要素を取り出すことができるメソッドです。<br>

```ruby
# 配列を作成します
array = [0,1,2,3,4,5,6]

# 配列から引数で指定した要素を取得します
ele1 = array.slice(1)
puts ele1
#=> 1  # 0番目から始まるため、1が取り出されました

# 配列番号-4から4つ分の要素をsliceします
ele2 = array.slice(-4,4)
puts ele2
#=> 3, 4, 5, 6

# 配列はもとのままです
puts array 
#=> [0,1,2,3,4,5,6]
```
