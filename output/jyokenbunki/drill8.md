# if,elseを使ったプログラムを作成

2桁の正の整数を入力します。<br>
その整数が、10の倍数（10,20,30...）からの差が2以内であるときはTrue、<br>
それ以外はFalseと出力するメソッドを作りましょう。<br>

```ruby
def near_ten(num)
  quotient = num % 10
  if quotient <= 2 || quotient >= 8
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
near_ten(12)
```

```ruby
# ターミナル
True
```

# 解説
2桁の整数を10で割ったときの余り = quotient<br>
if文では、その余り（quotient）が、２以下か８以上のとき"True"か"False"を出力するよう記述しています。<br><br>

今回は2桁の数字が12です。<br>
12 % 10 = 2<br>
2以下であるため、Trueが返されました。<br>

