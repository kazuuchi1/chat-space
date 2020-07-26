## User_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|name|integer|null: false, foreign_key: true|
|e-mail|integer|null: false, foreign_key: true|

### Association
has_many :group
has_many :message

## Group_groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|name|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
has_many :message

## Message_messagesテーブル

|Column|Type|Options|
|------|----|-------|
|message_id|integer|null: false, foreign_key: true|
|body|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|name|integer|null: false, foreign_key: true|
|image|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group
