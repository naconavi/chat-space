##usersテーブル

This README would normally document whatever steps are necessary to get the
application up and running.
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, add_index: true|
|email|string|null: false, unique: true|

Things you may want to cover:
##Association
- has_many :messages
- has_many :groups_users
- has_many :groups, through: groups_users

* Ruby version
##messageテーブル

* System dependencies
|Column|Type|Options|
|------|----|-------|
|body|text|
|image|string|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

* Configuration
##Association
- belongs_to :group
- belongs_to :user

* Database creation
##groupsテーブル

* Database initialization
|Column|Type|Options|
|------|----|-------|
|group_name|string|null: false, unique: true|

* How to run the test suite
##Association
- has_many :messages
- has_many :groups_users
- has_many :users, through: groups_users

* Services (job queues, cache servers, search engines, etc.)
##groups_usersテーブル

* Deployment instructions
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

* ...
## Association
- belongs_to :group
- belongs_to :user
