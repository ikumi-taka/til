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

## ちょっと復習...
1. ハッシュから特定の値を取得するときは、その値に対応するキーを指定する必要があります。
ハッシュ[取得したい値のキー]

1. # hash = { キー: 値 }

- ハッシュのキーを取得する→keysメソッド
- 値を取得する→valuesメソッド
を使用します。

（例）<br>
```ruby
hash = {one: 1, two: 2, three: 3}
puts hash.keys
puts hash.values
```
```:ターミナル
one
two
three
1
2
3
```

## 解説

```ruby
movie = {"title" => "ハリーポッター", "genre" => "ファンタジー", "year" => "2001年"}
```
上記のように生成されたハッシュからバリューを取得したいときは、キーを***文字列***で指定します。<br>
ハリーポッターという「バリュー」を取り出したいときは、movie["title"]とします。<br>

```ruby
movie = {title: "ハリーポッター", genre: "ファンタジー",  year: "2001年"}
```
例えば、上記のようなハッシュからバリューを取得する場合、movie[:title]と書きます。<br>
（シンボル[:]を使う。）<br>
