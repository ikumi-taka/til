# クラス・インスタンスを利用してプログラムを作成しよう
条件は以下の通りです。
- Bookクラスを作成する
- Bookクラスは@titleと@priceをプロパティとして持っている
- attr_readerを使用する
- Bookクラスのインスタンスを作成する（タイトル、価格は任意）
- 作成したインスタンスから、タイトルと価格を取得し画面に表示させる。

## attr_readerとは？
attr_readerメソッドとは、主に記述量を減らすために活用されます。<br>
インスタンス変数を呼び出すメソッドを定義するメソッドです。<br>
以下（例1）（例2）は結果は同じとなりますが、記述量に差があります。<br>

（例1）
```ruby
# attr_readerを使用しない場合
class Dog
  def initialize(name)
    @name = name
  end

  def name
    @name
  end

end

dog = Dog.new("ポチ")
puts dog.name
```
（例2）
```ruby
# attr_readerを使用した場合
class Dog
  attr_reader :name

  def initialize(name)
    @name = name
  end
end

dog = Dog.new("ポチ")
puts dog.name
```

それでは問題に移ります。
```ruby
# 自分の回答
class Book
  attr_reader :title, :price

  def initialize(title, price)
    @title = title
    @price = price
  end
end

book = Book.new("プログラミングについて", 3000)
puts book.title
puts "#{book.price}円"
```

```ruby

# 模範回答
class Book
  attr_reader :title, :price

  def initialize(title, price)
   @title = title
   @price = price
  end
end

book = Book.new("プロを目指す人のためのRuby入門", 3218)
puts book.title
puts "#{book.price}円"
```
## 解説
```ruby
attr_reader :title, :price
```
上記コードを書くことで、@titleと@priceにアクセスすることができます。<br>
ちなみに、attr_readerを使わない場合の回答は以下のようになります。<br>
```ruby
# attr_readerを使わない場合
class Book

  def initialize(title, price)
   @title = title
   @price = price
  end

  def title
    @title
  end

  def price
    @price
  end

end

book = Book.new("プロを目指す人のためのRuby入門", 3218)
puts book.title
puts "#{book.price}円"
```







