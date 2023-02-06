# インスタンスの生成を行ってプログラムをつくる

ターミナルで、以下のように出力されるようプログラムを作っていきます。

```ruby
採れたて新鮮な果実です
リンゴは120円です
オレンジは200円です
イチゴは60円です
# ターミナル
```


```ruby
class Fruit

  def self.fresh
    puts "採れたて新鮮な果実です"
  end

  def initialize(name, price)
    @name = name
    @price = price
  end

  def introduce
    puts "#{@name}は#{@price}円です"
  end
  end

  apple = Fruit.new("リンゴ", 120)
  orange = Fruit.new("オレンジ", 200)
  strawberry = Fruit.new("イチゴ", 60)

  Fruit.fresh
  apple.introduce
  orange.introduce
  strawberry.introduce
```

## 解説
この問題は、もともと条件提示と雛形があり、それに沿って作成していく問題でした。<br>
作成手順を書いていきたいと思います。
- インスタンスを生成し、インスタンス変数の定義を行います。<br>
インスタンスを生成するときに引数を書くこと。<br>
そして、nitializeメソッドについて覚えているか？→忘れていました。<br>
これはnewメソッドの引数を受け取ることができるメソッドです。<br>
なので、以下のように書きます。

```ruby
def initialize(name, price)
  @name = name
  @price = price
end

# メソッド外
apple = Fruit.new("リンゴ", 120)
orange = Fruit.new("オレンジ", 200)
strawberry = Fruit.new("イチゴ", 60)
```

- クラスメソッドfreshを定義します

下記のようにしてクラスメソッドを定義します。<br>
```ruby
class クラス名
  def self.メソッド名
    # 処理
  end
end

# クラスメソッドの呼び出し
クラス名.メソッド名(引数)
```

```ruby
def self.fresh
  puts "採れたて新鮮な果実です"
end
```
putsの内容は、条件で指定があったためこのように書きました。<br>

- インスタンスメソッドを定義します

```ruby
def introduce
   puts "#{@name}は#{@price}円です"
end
```

- クラスメソッドとインスタンスメソッドを呼び出します<br>

クラスメソッド：クラス名.メソッド名<br>
インスタンスメソッド：インスタンス.メソッド名<br>

```ruby
Fruit.fresh
apple.introduce
orange.introduce
strawberry.introduce
```


