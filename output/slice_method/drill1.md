# slice!メソッドを使って任意の文字列を部分的に削除するプログラムの作成

条件は以下の通りです。
- 対象となる文字列からn番目の文字を削除すること
- 削除された文字以外の文字列を出力すること


```ruby
def string(str, n)
  str.slice!(n - 1)
  puts str
end

# 以下は呼び出し例
string('Helloworld', 1)
string('Helloworld', 2)
string('Helloworld', 4)
```

## 解説
stringメソッドの引数strは、<br>
対象となる文字列（今回だと、Helloworld）、nは○番目の文字を消すのかを指示する数字が入ります。<br>
2行目の(n - 1)についてですが、先頭の文字列は0番目としてカウントされてしまうため、-1を付け加えています。<br>
