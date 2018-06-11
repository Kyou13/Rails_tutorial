# README
## 1章
- init
```
rails new
bundle install --path vendor/bundler --without production //以後記憶
```
gemfile
```aidl
group development test
gem sqlite3

group production
gem pg
```

## 2章
scaffoldでマイクロtwitterさくせい
- scaffold
    - MVCからルートまで全部やってくれる
    
- Usersリソース作成    
```aidl
rails g scaffold User name:string mail:string //単数
```    
- Micropostsリソース作成
```aidl
rails g scaffold Micropost content:text user_id:integer //単数
```
- model/micropost.rbにバリデーション追加
```
validates :content, length: {maximum: 140}, presence: true //複数
```    

Controller 複数
model 単数
### heroku の流れ
```aidl
heroku create <app name>
git add remote heroku 

```
- DBリセット
```
heroku pg:reset DATABASE
```
    
## TODO    
- Requestsで完結に書く
- filterで画像つき
- user_url(@user) でなぜ
