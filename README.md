# README

## users テーブル
| Column             | Type    | Options             |
| ------------------ | ------- | ------------------- |
| email              | sting   | null: false, unique |
| encrypted_password | string  | null: false         |
| name               | string  | null: false         |
| profile            | text    | null: false         |
| occupation         | text    | null: false         |
| position           | text    | null: false         |

### Association


## prototypes テーブル

| Column     | Type       | Options                        |
| ---------- | ---------- | ------------------------------ |
| title      | sting      | null: false                    |
| catch_copy | text       | null: false                    |
| concept    | text       | null: false                    |
| user       | references | null: false, foreign_key: true |

## comments テーブル

| Column    | Type       | Options                        |
| --------- | ---------- | ------------------------------ |
| content   | text       | null: false                    |
| prototype | references | null: false, foreign_key: true |
| user      | references | null: false, foreign_key: true |