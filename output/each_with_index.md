# each_with_index
each_with_indexはRubyに標準で組み込まれているメソッドです。
繰り返し処理をしながら、その要素が何番目に処理されたのか、表示することができます。

```ruby
配列名.each_with_index  do |item, i|

end
```

例
```ruby
animals = ["ねこ", "とり", "うさぎ"]

animals.each_with_index do |animal, i|
  puts "#{i + 1}番目の動物は、#{animal}です"
end
```

```
1番目の動物は、ねこです
2番目の動物は、とりです
3番目の動物は、うさぎです
# ターミナル出力
```

配列は0番目から始まるため、#{i + 1}としています。
