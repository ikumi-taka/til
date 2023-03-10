# Rails deviseの導入
```ruby
# Gemfile
gem 'devise'
```

```ruby
# ターミナル
bundle install
```

```ruby
# ターミナル
rails s
```
```ruby
# ターミナル
rails g devise:install
```

## 補足
運用やテスト、本番全ての環境で使用するため、gem 'devise'は一番下に記述。<br>
bundle install後は、基本的にサーバーの再起動が必須。<br>
rails g devise:installコマンドを実行することで、deviseの設定ファイルをrailsアプリケーションにインストールします。<br>
これによって、使用するファイルが自動で生成されます。<br>

## ChatGPTにも聞いてみた
最近ChatGPTのアカウントを作ったので、試しにrailsのdevise導入手順について聞いてみました。
[![Image from Gyazo](https://i.gyazo.com/8122d53360b6ffea7da4e2f2c36e1feb.gif)](https://gyazo.com/8122d53360b6ffea7da4e2f2c36e1feb)

説明とコマンドの両方記載してくれていました。
色々なこと試してみると面白いかもしれませんね。
