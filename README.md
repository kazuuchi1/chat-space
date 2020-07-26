## User_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false|
|name|integer|null: false|
|e-mail|integer|null: false|

### Association
- has_many :group
- has_many :message

## Group_groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false|
|user_id|integer|null: false, foreign_key: true|
|name|integer|null: false|

### Association
- belongs_to :group
- has_many :message

## Message_messagesテーブル

|Column|Type|Options|
|------|----|-------|
|message_id|integer|null: false|
|body|integer|null: false|
|user_id|integer|null: false, foreign_key: true|
|name|integer|null: false|
|image|integer|null: false|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group
