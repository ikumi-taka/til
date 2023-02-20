# sliceメソッドを使って2つの文字列の末尾に対して、一致しているかどうかを判断するプログラムを作ります

- メソッドの引数に、任意の2つの文字列を指定する。
- 引数に指定された2つの文字列のうち、どちらかがもう一方の文字列の末尾にある場合は、Trueを出力する
- 上記を満たせていない場合は、Falseを出力する
- 入力された文字が大文字でも小文字でも、同一の文字として処理を行う

ヒント1:sliceメソッドを活用する<br>
ヒント2:大文字を小文字に変換するdowncaseメソッドを利用する<br><br>


```ruby:模範解答
def end_other(a, b)
  a_down = a.downcase
  b_down = b.downcase
  a_len = a_down.length
  b_len = b_down.length
  if b_down.slice(-(a_len)..- 1) == a_down || a_down.slice(-(b_len)..- 1) == b_down
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
end_other('Hiabc', 'abc') 
```

```:ターミナル
True
```

# 解説
今回、条件の中に大文字と小文字を区別しないと記載があったため、２つの任意の文字列を小文字に変換させます。<br>
次に、2つの文字列のうち、どちらかがもう一方の文字列の末尾にあるかどうか確かめるため、a, bそれぞれの文字数を数えます。<br>
それが以下の記述になります。<br>

```ruby
  a_down = a.downcase
  b_down = b.downcase
  a_len = a_down.length
  b_len = b_down.length
```


```ruby:呼び出し例
end_other('Hiabc', 'abc') 
```
ここからは、呼び出し例が上記だった場合を例に考えて行きます。<br>
この場合、以下のように処理がされます。<br>
```ruby
a_down = hiabc
b_down = abc
a_len = 5
b_len = 3
```

if分の中身を見ていきます。<br>
< 条件式の左辺 ><br>
b_down.slice(-(a_len)..- 1)は、b_down.slice(-5..-1)となりますが、b_down = abcとなっているため、インデックス番号-5から-1という条件で切り取ることができません。<br>
そのため、この部分はnilとなります。<br>
結果、nil == a_downは等しくないと評価されるので、falseになります。<br><br>

< 条件式の右辺 ><br>
a_down.slice(-(b_len)..- 1)はと、a_down.slice(-3..-1)となります。<br>
ここで、hiabcという文字列の最後にabcが含まれているかを確認したいため、abcという文字列分を左から数えます。<br>
そうするとhiabcの最後までを範囲指定していることがわかります。<br>
a_down = hiabcとなるので、インデックス番号-3から-1という条件で切り取るとabcが残ります。<br>
結果、abc == b_downは等しいと評価されるので、trueとなります。<br>
