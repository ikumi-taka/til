# 引数とハッシュを使ってプログラムを作成する

[ 問題 ]<br>
ある映画のハッシュを定義し、格納されている「title」(タイトル）・「genre」(ジャンル)・「year」(公開年)の三つの要素の中から一つを取り出すプログラムを作成してください。<br><br>

定義する変数<br>
①movie = {"title" => "ハリーポッター", "genre" => "ファンタジー", "year" => "2001年"}<br><br>

②ユーザーが入力するキーを、getsメソッドを利用し定義しましょう<br>

```ruby
# 模範回答
def movie_info(movie, data)
  puts movie[data]
end

movie = {"title" => "ハリーポッター", "genre" => "ファンタジー", "year" => "2001年"}

puts "以下から一つを選んで入力してください。
  ・title
  ・genre
  ・year"

info = gets.chomp

movie_info(movie, info)
```
