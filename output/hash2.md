- ハッシュから特定の値を取得するときは、その値に対応するキーを指定する必要があります。

```
ハッシュ[取得したい値のキー]
```

- 二重ハッシュから特定の値を取得するときは、取得したい値のキーまで連続して指定する必要があります。

```
ハッシュ[取得したい値のキー][取得したい値のキー]
```

例
```ruby
user_data = [
 {user: {profile: {name: 'George'}}},
 {user: {profile: {name: 'Alice'}}},
 {user: {profile: {name: 'Taro'}}},
]
```
上記、複数のユーザーの情報をハッシュとして持つ変数があります。
全てのユーザーの名前だけが出力されるようにコーディングする場合どうしたら良いか？

模範解答
```ruby
user_data.each do |u|
  puts u[:user][:profile][:name]
end
```
あるいは
```ruby
user_data.each{ |u| puts u.dig(:user, :profile, :name) }
```
