# usersテーブル

|Column|Type|Options|
|------|:-------:|-------:|
|email|string|null:false,ユニーク|
|encrypted_password|string|null:false|
|name|string|null:false|
|profile|text|null:false|
|occupation|text|null:false|
|position|text|null:false|

## Association
- has_many :protptypes
- has_many :comments


# prototypeテーブル
|Column|Type|Options|
|-|:-:|-:|
|title|string|null:false|
catch_copy|text|null:false
concept|text|null:false
user|references|null:false,外部キー


## Association
- belongs_to :user
- has_many :comments


# commentsテーブル
|Column|Type|Options|
|-|:-:|-:|
content|text|null:false
prototype|references|null:false
user|references|null:false,外部キー


## Association
- belongs_to :user
- belongs_to :prototype

