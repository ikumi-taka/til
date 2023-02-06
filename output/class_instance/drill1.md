
ターミナルで以下のように出力させるために、コーディングしていきます。<br>

```
# ターミナル
著者: 太郎
タイトル: プログラミングについて
本文: プログラミングを学ぼう！
```

```ruby
class Article

  def initialize(author, title, content)
    @author = author
    @title = title
    @content = content
  end

  def author
    @author
  end

  def title
    @title
  end

  def content
    @content
  end
end
article = Article.new("太郎", "プログラミングについて", "プログラミングを学ぼう!")

puts "著者: #{article.author}"
puts "タイトル: #{article.title}"
puts "本文: #{article.content}"
```
***Article.new***で変数articleに代入しています。
（）の中に実引数。

initializeメソッド内に、インスタンス変数を宣言しています。
インスタンス変数は頭に@がつきますね。

("太郎", "プログラミングについて", "プログラミングを学ぼう!")
この３つの値が、initializeメソッドで宣言されたインスタンス変数（@author, @title, @content）に代入されます。

```ruby
def author
    @author
  end

  def title
    @title
  end

  def content
    @content
  end
  ```
この部分は、インスタンス変数の値を返すための専用メソッドを定義しています。

最後のputs3行は、定義したメソッドを呼び出して、ターミナルに出力されるようになっています。

# initializeメソッド
initializeメソッドとは、インスタンスが定義されたときに、そのインスタンスが自動的に実行処理を定義するインスタンスメソッドです。
