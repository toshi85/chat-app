## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|index: true,,null: false|
### Association
- has_many :messages
- has_many :comments

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user|string|index: true,null: false|
### Association
- has_many :messages
- has_many :comments

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user

## commentsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text||
|user_id|integer|null: false, foreign_key: true|
|message_id|integer|null: false, foreign_key: true|
