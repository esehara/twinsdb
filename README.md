twinsdb
=======

NoSQL, specific bidirectional database

What is twinsdb?
================

twinsdb look likes Key-Value Store, but is a bit different. This is a bidirectional database.

Often, many key-value stores get Value from Key, but cannot get Key from Value.

```
A -> B
B ?> A
```

It is not neccessary to distinguish between Key and Valuem and only key-pair, and bidirectionaly get.

```
A -> B
B -> A
```


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


