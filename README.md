# README

Clone the repo

```
git clone git@github.com:eileencodes/migration_bug_demo.git
```

Run setup script

```
bin/setup
```

Checkout the branch linked to master rails branch

```
git checkout rails-master
```


Run setup script again

```
bin/setup
```

You will see the following error when the script hits db:seed


```
ActiveRecord::NotNullViolation: Mysql2::Error: Field 'id' doesn't have a default value: INSERT INTO `posts` (`title`, `created_at`, `updated_at`) VALUES ('This is a title', '2016-12-15 16:45:01', '2016-12-15 16:45:01')
/Users/eileen/Sites/open_source/rails_apps/migration_test_app/db/seeds.rb:9:in `<top (required)>'
bin/rails:4:in `require'
bin/rails:4:in `<main>'
Mysql2::Error: Field 'id' doesn't have a default value
/Users/eileen/Sites/open_source/rails_apps/migration_test_app/db/seeds.rb:9:in `<top (required)>'
bin/rails:4:in `require'
bin/rails:4:in `<main>'
Tasks: TOP => db:seed
```
