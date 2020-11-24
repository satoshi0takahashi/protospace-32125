# Table detail

# Users

|Column    |Type      |Options
|----------|----------| ---------|
|email     |string    |Null: false|
|password  |string    |Null: false|
|name      |string    |Null: false|
|profile   |text      |Null: false|
|occupation|text      |Null: false|
|position  |text      |Null: false|

## Association
- has_many :prototypes
- has_many :comments

# Prototypes
|Column    |Type      |Options
|----------|----------| ---------|
|title     |string    |Null: false
|catch_copy|text      |Null: false|
|concept   |text      |Null: false|
|image     |Active Storage||
|user      |reference |foreign key: true|

## Association
- belongs_to :users
- has_many :comments

# Comments
|Column    |Type      |Options
|----------|----------| ---------|
|text     |text    |Null: false|
|user  |reference   |foreign key:true|
|prototype      |reference   |foreign key:true|

## Association
- belongs_to :user
- belongs_to :prototypes