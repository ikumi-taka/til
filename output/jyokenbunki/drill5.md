# if, else問題

Aさんは普段土日が休みの仕事に就いており、休みの日は遅くまで寝ていたいと考えています。<br>
そこで、Aさんのために「その日が遅くまで寝ていられるかどうか」を判断するプログラムを作成します。<br><br>

第一引数の値では「平日かどうか」、第二引数の値では「休暇かどうか」をtrueまたはfalseを用いて以下のように表します。
- 条件1:第一引数がtrue（平日である）または、第二引数がtrue（休暇である）の場合はtrueと出力する
- 条件2:第一引数がfalse（平日でない）または、第二引数がtrue（休暇である）の場合はtrueと出力する
- 条件3:第一引数がtrue（平日である）または、第二引数がfalse（休暇でない）の場合はfalseと出力する
- 条件4:第一引数がfalse（平日でない）または、第二引数がfalse（休暇でない）の場合はtrueと出力する

```ruby
def sleep_in(is_weekday, is_vacation)
  if (is_weekday != true) || (is_vacation == true)
    puts true
  else
    puts false
  end
end

# 呼び出し例
sleep_in(false, false)
```

## 解説

- 第一引数「平日かどうか」<br>
平日：true<br>
平日ではない：false<br>

- 第二引数「休暇かどうか」<br>
休暇：true<br>
休暇ではない：false<br>

今回の条件から、「平日ではない」もしくは「平日だけど休暇」という場合がtrue。<br>
「平日であり」、「休暇でもない」場合はFalse。<br><br>

「〜ではない」という記述の仕方は否定の演算子!=を使います。<br>
||は「または」という意味を表現しています。<br>

