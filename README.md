# テーブル設定

## usersテーブル

｜ Column     | type   | options   |
｜ ---------- | ------ | --------- |
｜ email      | string | NOT: NULL |
｜ password   | string | NOT: NULL |
｜ name       | string | NOT: NULL |
｜ profile    | text   | NOT: NULL |
｜ occupation | text   | NOT: NULL |
｜ position   | text   | NOT: NULL |

### Association

- has_many :prottypes
- belongs_to :comments

## prototypesテーブル

｜ Column     | type       | options   |
｜ ---------- | ------     | --------- |
｜ title      | string     | NOT: NULL |
｜ catch_copy | text       | NOT: NULL |
｜ concept    | text       | NOT: NULL |
｜ image      |            |           |
｜ user       | references |           |

### Association

- belongs_to :users
- has_many :comments

## comments

｜ Column     | type       | options   |
｜ ---------- | ---------- | --------- |
｜ text       | text       | NOT: NULL |
｜ user       | references |           |
｜ prottype   | references |           |


### Association

- has_many :users
- has_many :prototypes
