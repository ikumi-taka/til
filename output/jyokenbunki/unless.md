# 条件分岐処理

## unless文
「もし〇〇だったら□□をする」という処理をします。<br>
unless文はif文と反対で、条件式が「偽(false)」の時に処理が実行されます。
unless文にelsif を指定することはできないです。

公式リファレンスを参考にしました。
https://docs.ruby-lang.org/ja/latest/doc/spec=2fcontrol.html#unless

```ruby
unless 条件式
  処理1（条件式がfalseのときに実行）
else
  処理2（条件式がtrueのときに実行）
end
```
unless文は、条件式が「正しい」か「正しくないか」で実行する処理を分岐させています。<br>
***「正しい」 = true***<br>
***「正しくないか」 = false***<br>
条件式が正しくない（false）なら、処理1を実行。<br>
条件式が正しい（true）なら、処理2を実行。<br>
