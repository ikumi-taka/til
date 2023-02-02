# include?メソッド
指定した値が配列や文字列内に含まれているかを判定するメソッドです。<br>
指定した値が含まれている→true<br>
指定した値が含まれていない→false　　を返り値として返します。<br>

例1
```ruby
string = ["hello", "goodbye"]
puts string.include?("hello")
```

```
true
# ターミナル出力
```
例2
```ruby
string = ["hello", "goodbye"]
puts string.include?("thanks")
```

```
false
# ターミナル出力
```
