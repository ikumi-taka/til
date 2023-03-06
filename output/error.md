# Ruby on Rails アプリ作成 序盤に出たエラー
# はじめに
新しくアプリケーションを立ち上げて
```ruby
rails db:create
```
を実行したときにでたエラーを解決したため、忘れないうちに記録したいと思い投稿します。

# どんなエラーが出たのか
```ruby:実行していたこと①
rails _6.0.0_ new xxx -d mysql
```

```ruby:実行していたこと②
rails db:create
```

そうすると、以下のようなエラーが出ました。
```:ターミナル
/Users/admin/.rbenv/versions/2.6.5/lib/ruby/2.6.0/net/protocol.rb:66: warning: already initialized constant Net::ProtocRetryError
/Users/admin/.rbenv/versions/2.6.5/lib/ruby/gems/2.6.0/gems/net-protocol-0.2.1/lib/net/protocol.rb:68: warning: previous definition of ProtocRetryError was here
/Users/admin/.rbenv/versions/2.6.5/lib/ruby/2.6.0/net/protocol.rb:206: warning: already initialized constant Net::BufferedIO::BUFSIZE
/Users/admin/.rbenv/versions/2.6.5/lib/ruby/gems/2.6.0/gems/net-protocol-0.2.1/lib/net/protocol.rb:214: warning: previous definition of BUFSIZE was here
/Users/admin/.rbenv/versions/2.6.5/lib/ruby/2.6.0/net/protocol.rb:503: warning: already initialized constant Net::NetPrivate::Socket
/Users/admin/.rbenv/versions/2.6.5/lib/ruby/gems/2.6.0/gems/net-protocol-0.2.1/lib/net/protocol.rb:541: warning: previous definition of Socket was here
Created database 'xxx_development'
Created database 'xxx_test'
```

自分にとってこのエラーは初めて見た文章でした。

- already initialized constant Net::ProtocRetryError<br>
→すでに初期化されている定数 Net::ProtocRetryError<br><br>

- warning: previous definition of ProtocRetryError was her<br>
→ 警告: ProtocRetryError の以前の定義は彼女のものでした<br><br>

- warning: already initialized constant Net::BufferedIO::BUFSIZE<br>
→　警告: BUFSIZE の以前の定義はここにありました<br><br>

- lready initialized constant Net::NetPrivate::Socket<br>
→既に初期化された定数 Net::NetPrivate::Socket<br><br>

- warning: previous definition of Socket was here<br>
→警告: Socket の以前の定義はここにありました<br><br>

Google翻訳で訳してもらいましたが、あまりピンと来ない、、。<br>
そこで、同じようなエラーを解決した記事を見つけたので、そちらを参考に解決までの手順を書いて行きます。<br>


# 実行したこと
Gemfileに以下を追記しました。
```ruby:Gemfil
gem 'net-http'
```
その後、サーバーを再起動（rails s）すると、これまで出てきていたエラーが表示されなくなり、無事に解決しました。<br>


# 参考文献

https://wakunkyo.com/net-protoc-retry-error/

https://zenn.dev/tarou_yuruyuru/articles/163f5b734409f7

ありがとうございました。
