### Searchlogic
---

https://github.com/binarylogic/searchlogic

```
sudo gem install searchlogic
script/plugin install git:github.com/binarylogic/searchlogic.git


```

```rub
User(id: integer, created_at: datetime, username: string, age: integer)
User.username_equals("bjohnson")

scope = User.username_like("bjohnson").age_greater_than(20).id_less_than(55)
scope.all
scope.first
scope.count

User.username_is(10)

User.has_many :orders

LineItem.named_scope :expensive, :conditions => "line_items.price > 500"

Audit.belongs_to :auditable, :polymorphic => true
User.has_many :audits, :as => :auditable
Audit.auditable_user_type_username_equals("ben")

Benchmark.bm do |x|
  x.report { 10.times { Event.tickets_id_gt(10).all(:include => :tickets) } }
  x.report { 10.times { Evnet.tickes_id_gt(10).all } }
end



```

```
```

