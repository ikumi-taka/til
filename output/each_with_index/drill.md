# searchメソッドとeach_with_indexメソッドを組み合わせてプログラムを作る

```ruby
def search(target_num, input)

  input.each_with_index do |num, i|
    if num == target_num
      puts "#{i + 1}番目にあります"
      return
    end
  end
  puts "その数は含まれていません"
end

input = [2, 4, 6 ,8, 10, 12, 14, 16, 18, 20]
search(10, input)
```

↓配列inputを定義しています。<br>
input = [2, 4, 6 ,8, 10, 12, 14, 16, 18, 20]<br><br>

↓searchメソッドを呼び出しています。10と変数inputは実引数。<br>
search(10, input)<br><br>

1行目、呼び出されたsearchメソッドでは、target_numとinputを借り引数として受け取ります。<br>

input.each_with_index〜内での処理<br>
配列inputに格納されている要素を１つ一つnumとして取り出し、要素ごとに当てられている添字をindexで取得します。<br>
if文でnumとtarget_numが等しいと、「○番目にあります」とターミナルで出力されます。<br>
returnでそのメソッドを終わらせます。<br>
