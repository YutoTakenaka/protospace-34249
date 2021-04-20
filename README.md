 テーブル設計

## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| email    | string | null: false |
| password | string | null: false |
| name     | string | null: false |
| profile  | text   | null: false |
|occupation| text   | null: false |
| position | text   | null: false |

### Association

- has_many : prototypes
- has_many : comments

## prototypes テーブル
| Column | Type   | Options     |
| ------ | ------ | ----------- |
| title  | string | null: false |
| catch_copy| text| null: false |
|concept | text   | null: false |
| image  |        |             |
| user   | references |             |

### Association

- has_many : comments
- belongs_to : users

## comments テーブル

| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| text   | text       | null: false |
| user   | references |             |
| prototype | references |          |
### Association

- belongs_to :prototypes
- belongs_to :user
