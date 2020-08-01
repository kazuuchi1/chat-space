## Userテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|e_mail|integer|null: false|

### Association
- has_many :messages
- has_many :groups_users
- has_many :groups, through: :groups_users

## Groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|integer|null: false|

### Association
- has_many :messages
-has_many :groups_users
-has_many :users, through: :groups_users

## Message_messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|
|user_id|text|null: false, foreign_key: true|
|image|string|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group

## Groups_users

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group