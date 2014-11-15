## README

How to create sandbox
```
bundle install
bundle ex rake db:migrate
rails c

```
You can reproduce the issue following..

```
a = Person.create
3.times {a.books.build.save}
a.books.where(id: 1).destroy_all
#=>ArgumentError: wrong number of arguments (1 for 0)
```
