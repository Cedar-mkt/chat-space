# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|username|string||
|email|string|null :false, unique :true|
|password|string|null :false|
### Association
- has_many :groups
- has_many :messages


## groups テーブル
|Column|Type|Options|
|------|----|-------|
|groupname|string|null :false|
### Association
- has_many :users

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null :false, foreign_key :true|
|group_id|integer|null :false, foreign_key :true|
### Association
- belongs_to :user
- belongs_to :group


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|string|null :false|
|image|string||
|timestamps||null :false|
|user_id|integer|null :false, foreign_key :true|
|group_id|integer|null :false, foreign_key :true|
### Association
- belongs_to :user


* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
