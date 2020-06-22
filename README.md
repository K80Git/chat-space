

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|name|string|null: false, foreign_key: true|
|email|string|null: false, foreign_key: true|
|encrypted_password|string|null: false, foreign_key: false|


## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false|
|group_name|string|null: false|
|group_member|integer|null: false, foreign_key: true|

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false, foreign_key: true|
|image|string|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
