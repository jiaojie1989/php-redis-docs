PHP Redis HASH Operation Methods
===
# HSET
```PHP
$redis->hSet($key, $field, $value);
```
* VERSION >= 2.0.0
* O(1)
* RETURN
** `1` if field is a new field in the hash and value was set.
** `0` if field already exists in the hash and the value was updated.

# HGET
```PHP
$redis->hGet($key, $field);
```
* VERSION >= 2.0.0
* O(1)
* RETURN
** the value associated with field if exists.
** `false` when field is not present in the hash or key does not exist.
