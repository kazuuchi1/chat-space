## User_usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|e_mail|integer|null: false|

### Association
- has_many :groups
- has_many :message

## Group_groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false|
|name|integer|null: false|

### Association
- belongs_to :group
- has_many :messages

## Message_messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|integer|
|user_id|text|null: false, foreign_key: true|
|image|integer|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group

## Groups_users

|Column|Type|Options|
|------|----|-------|
|group|integer|null: false, foreign_key: true|
|user|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group