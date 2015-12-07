PHP Redis HASH Operation Methods
===
# HSET
```PHP
$redis->hSet($key, $field, $value);
```
* `VERSION` >= `2.0.0`
* O(`1`)
* RETURN
  * `1` if field is a new field in the hash and value was set.
  * `0` if field already exists in the hash and the value was updated.

# HGET
```PHP
$redis->hGet($key, $field);
```
* `VERSION` >= `2.0.0`
* O(`1`)
* RETURN
  * `Bulk string reply` the value associated with field if exists.
  * `false` when field is not present in the hash or key does not exist.

# HINCRBY
```PHP
$redis->hIncrBy($key, $field, $increment);
```
* `VERSION` >= `2.0.0`
* O(`1`)
* RETURN
  * `Integer reply` the value at field after the increment operation.
  * `false` when trying to increase another key type or a field already filled with non-numberic string, or some other thing that goes wrong.
* NOTICE
  * when trying to increase an unexisted key or field, the default value is `0`.
