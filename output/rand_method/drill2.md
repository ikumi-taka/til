# randとshuffleを使ってプログラムを作成
誕生日を入力すると、今日の運勢を表示してくれるプログラムを作ってください。
占い結果については、以下のアルゴリズムにて判定することとします。
必ず、メソッドを作成しそれを呼び出すように記述してください。

- 引数として誕生日の数字を受け取る(例：4月3日なら403、11月15日なら1115と入力)
- 誕生日の数字に、乱数で生成された0 ~ 9の数字のいずれかを掛け算し、その後4で割った時の余りを算出
- シャッフルした占い結果を格納した配列から、上記の数値の順番の値を取り出す
　["凶","中吉","吉", "大吉"]
 
※ヒント<br>
乱数を生成 = rand<br>
配列の要素をシャッフル = shuffle<br>

## shuffle使い方
```ruby
# shuffleメソッドで配列をシャッフルし、変数animalsに代入
animals = ["cat", "dog", "rabbit"].shuffle

puts animals
# => ["rabbit", "cat", "dog"]
```

```ruby
# 自分の回答
def uranai(birthday)
  results = ["凶","中吉","吉", "大吉"].shuffle
  num = birthday * rand(10) % 4
  puts "今日のあなたの運勢は#{results[num]}"
end

puts "誕生日を入力してください(例：4月3日なら403、11月15日なら1115と入力)"
birthday = gets.to_i
uranai(birthday)
```

```ruby
# 模範回答
def result_of_uranai(birthday)
  results = ["凶", "中吉", "吉", "大吉"].shuffle
  num = birthday * rand(10) % 4
  puts "今日のあなたの運勢は、#{results[num]}だよ！"
end

puts "誕生日を入力してください！"

birthday = gets.to_i
result_of_uranai(birthday)
```

## 解説
プログラムの組み立て方としてまず始めに書いたものは、誕生日を入力してもらう部分です。
```ruby
puts "誕生日を入力してください(例：4月3日なら403、11月15日なら1115と入力)"
birthday = gets.to_i
```
to_iメソッドは整数に変換するメソッドです。<br>
その後、uranaiメソッド内を記述していきました。<br>
変数resultsに占い結果の配列の値が入っていて、それらをshuffleします。<br>
入力してもらった誕生日の数字に、乱数で生成された0〜9の数字を掛け、4で割った余りの数字を算出・計算方法が下記の部分になります。<br>
```ruby
num = birthday * rand(10) % 4
```

最後に、計算結果を元に、占い結果を取得し、puts〜で出力します。
