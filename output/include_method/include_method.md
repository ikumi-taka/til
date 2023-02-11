# include?メソッド
include = 含む, 含める という意味。<br>
指定した値が配列や文字列内に含まれているかを判定するメソッドです。<br><br>
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

応用例:大文字小文字を区別せずに検索する
```ruby
string = "Hello World"
puts string.downcase.include?("hello world")
```
```ruby
true
# ターミナル出力
```
downcaseメソッドは、大文字を小文字に変換します。
