# 預金システムのアルゴリズム問題
銀行口座に10万円の預金残高があり、お金を引き出すプログラムを作成します。
- お金を引き出すwithdrawメソッドを作成する
- お金を引き出すと手数料110円かかり、「◯◯円引き落としました。残高は◯◯円です」と表示する（残高は手数料を引いた額を表示します）
- もし預金残高より多く引き落としたら「残高不足です」と表示する

```ruby
# 雛形
def withdraw(balance, amount)
  fee = 110　　# 手数料
# 引き落とし額と残高を表示する、もしくは残高より多く引き落としたら残高不足と表示
end

balance = 100000　　# 残高
puts "いくら引き落としますか？（手数料110円かかります）"
money = gets.to_i
withdraw(balance, money)
```

```ruby
# 自分の解答
def withdraw(balance, amount)
  fee = 110  # 手数料
  if (amount + fee) <= balance
    puts "#{(amount + fee)}円引き落としました。残高は#{balance - (amount + fee)}円です"
  else
    puts "残高不足です"
  end
end

balance = 100000  # 残高
puts "いくら引き落としますか？（手数料110円かかります）"
money = gets.to_i
withdraw(balance, money)
```

```ruby
#　模範解答
def withdraw(balance, amount)
  fee = 110
  if balance >= (amount + fee)
    balance -= (amount + fee)
    puts "#{amount}円引き落としました。残高は#{balance}円です"
  else
    puts "残高不足です"
  end
end

balance = 100000
puts "いくら引き落としますか？（手数料110円かかります）"
money = gets.to_i
withdraw(balance, money)
```

100000円以下出金する場合は以下のように返ってきました。
```ruby
# ターミナル
いくら引き落としますか？（手数料110円かかります）
9890
10000円引き落としました。残高は90000円です
```

100000円以上出金する場合は以下のように返ってきました。
```ruby
# ターミナル
いくら引き落としますか？（手数料110円かかります）
100000
残高不足です
```

# 解説
money = gets.to_i　で入力した数値 + 手数料110円が100000円以下であれば引き落としは可能。<br>
合計が100001円以上だと、残高不足と返されるように作っていきます。<br><br>

模範解答では、100000以上の場合は、balance -= (amount + fee)、<br>
つまりbalance = balance - (amount + fee)が処理され、最終的な返り値が出力されるようになっています。<br><br>

私の解答は、考え方は合っていたように思いますが、コードの書き方？可読性をもう少し考えて書く必要があったように思います。<br>
