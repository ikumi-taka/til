# 引数とは
メソッドに渡すことができる値のこと。<br>

# 実引数と仮引数
```ruby
def メソッド名(仮引数)
  # 処理
end

# メソッドの呼び出し
メソッド名(実引数)
```
メソッドを定義したときに（）内に記述しておき、処理に利用するときは***仮引数***。<br>
メソッドを呼ぶときに（）内に渡す値を記述するのが***実引数***があります。<br>

```ruby
def メソッド名(第一引数, 第二引数)
  # 処理
end

メソッド名(第一引数, 第二引数)
```
引数は複数利用されることがあります。<br>
そんなときは、（）内、左から順に第一引数、第二引数、第三引数...と呼びます。

<br>
<br>
例<br>

```ruby
def get_weather_forecast(weather)
  puts "明日の天気は#{weather}です"
end

get_weather_forecast("晴れ")
```
<br>

```
# ターミナル出力
明日の天気は晴れです
```

<br>
- この例の場合、実引数="晴れ"、仮引数=weatherですね。<br>
- 明日の天気は〇〇です。の、〇〇は、任意の文字列を表示したいため、引数を使います。<br>
- 〇〇には、メソッドの呼び出し元の引数に渡した文字列が表示されます。<br>
- 文字列を出力するために、get_weather_forecastメソッドを定義します。<br>
- 引数で渡した文字列を表示させた値です。<br>

