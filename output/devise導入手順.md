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
