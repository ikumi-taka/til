# indexメソッドを使ってプログラムを作成します

任意の文字列に"code"が、左から何文字目に出てくるかを返し、その数を出力するメソッドを作りましょう。<br><br>

呼び出し・出力例は以下のような形で行います。<br>
count_code("codexxcode") → 1（ターミナルの返し）<br>
count_code("aaacodebbb") → 4（ターミナルの返し）<br>
count_code("cozexxcode") → 7（ターミナルの返し）<br>



```ruby
def count_code(str)
  puts (str.index("code") + 1)
end

呼び出し例
count_code("codexxcode")
```

## 解説
about_index.mdファイルを見ながら解くと理解しやすいです。<br>
indexメソッドは文字列の先頭を0番目から数えて返します。<br>
そのため、検索を開始する位置を+1して、1番目からカウントしてもらうように記述しています。<br><br>


模範解答例として、以下でもプログラムは実行できます。<br>
第二引数である0を省略して記述したものが上記で書いたものです。<br>
```ruby
def count_code(str)
  puts str.index("code", 0) + 1
end
```
