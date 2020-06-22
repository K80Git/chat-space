

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false|
|name|string|null: false|
|email|string|null: false|
|encrypted_password|string|null: false|

has_many:messages
has_many:groups

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false|
|group_name|string|null: false|
|group_member|integer|null: false, foreign_key: true|
has_many:users
has_many:groups

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
belong_to:users
belong_to:groups