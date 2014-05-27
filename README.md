twinsdb
=======

NoSQL, specific bidirectional database

Draft
=====

set
---

```
> set "foo" "bar"
OK
```

find
-----

```
> set "foo" "bar"
OK
> find "foo"
"bar"
> find "bar"
"foo"
```

findall
--------
```
> set "egg" "spam"
OK
> set "egg" "milk"
OK
> find "egg"
"spam"
> findall "egg"
["spam", "milk"]
```

link
-----

```
> set "egg" "spam"
OK
> set "spam" "milk"
OK
> link "egg"
["egg", "spam", "milk"]
> link "milk"
["milk", "spam", "egg"]
```

node
----
```
> set "egg" "spam"
OK
> set "egg" "milk"
OK
> node "egg"
["egg", ["spam", "milk"]]
```


