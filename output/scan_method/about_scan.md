# scanメソッド
対象の要素から引数で指定した文字列を数え、配列として返します。

```ruby
def count_hi(str)
  puts str.scan("hi")
end

# 呼び出し例
count_hi('abc hi ho')
```

```ruby
hi
# ターミナル出力
```

scanの公式リファレンスです。<br>
https://docs.ruby-lang.org/ja/latest/method/String/i/scan.html
