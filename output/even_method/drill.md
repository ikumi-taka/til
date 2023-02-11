# even?メソッドを使って偶数血の取得をするプログラムを作成します
配列にある値の中から偶数の数をカウントして出力するメソッドを作ります。<br><br>

出力例：
```ruby
count_evens([2, 1, 2, 3, 4]) → 3
count_evens([2, 2, 0]) → 3
count_evens([1, 3, 5]) → 0
```

```ruby
def count_evens(nums)
  count = 0
  nums.each do |num|
    if num.even?
      count += 1
    end
  end
  puts count
end

count_evens([2, 1, 2, 3, 4])
```

```ruby
3
# ターミナルでの返し
```

## 解説
- count = 0
今回は、配列の中の偶数がいくつあるのかを数える必要があります。<br>
カウントした数を保持するための変数が必要なので、変数countを用意しました。<br><br>

変数countをeach文の処理に記述すると、処理が繰り返されるたびにcount = 0が実行されます。<br>
そして、countの数値が0に上書きされるという仕組みです。<br>

- each文内
配列の中にある数字をeach文で１つずつ取り出し、even?メソッドで偶数かどうかの判定をしてもらい、偶数だった場合はcountに1を足していきます。
