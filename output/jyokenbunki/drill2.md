# if文を使った条件分岐
以下の条件を満たすようプログラムを作成する。

- 条件1：第一引数のnumが1以上かつ10以下の範囲であればTrueを出力すること
- 条件2：第二引数のoutside_modeがTrueの場合は、第一引数numが条件範囲外でもTrueを出力すること
- 条件3：それ以外はFalseを出力すること

```ruby
def in1to10(num, outside_mode)
  if (num >= 1 && num <= 10) || outside_mode
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
in1to10(5,false)
in1to10(11,false)
in1to10(11,true)
```
```ruby
True
False
True
# ターミナル出力
```

複数の条件がある場合は、***論理演算子***を使って記述を行います。
## 論理演算子とは
「真（true）」と「偽（false）」の確認を行う時に使われる演算子（記号）をのこと。<br>
複数の条件式を組み合わせて条件式を記述するときは、論理演算子&&や||を使います。<br>

例
```ruby
# aもbもtrueの場合にtrue
a && b 

# aかbのどちらかがtrueの場合にtrue
a || b 
```










