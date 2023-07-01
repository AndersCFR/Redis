# Redis Fundamentals


## Keys

Unique keys, it can be flat namespace, should be up to 512 MB

Main commands: 

> SET <key> <value> [EX] [NX],

>> SET user:1000:time-zone "UTC-8" EX 7200,

>>> Set user time zone woth expiraton of 7200 seconds

> GET <key>

>> GET user:1000:time-zone

> DEL, 

> UNLINK (delete, memory is claimed in an async way)

A key name can be made of any sequence of bytes

It is possible to set expiration times.


## Strings

It is the basic data structure. Can be used to store anything in string format, numbers, json, csv, 
images even audio files

Can work with number and use increment or decrement.

## Hashes

They are mutable, looks like a Python dictionary, O(n) complexity. Store extremely efficiently.


> dbsize

>> Get number of keys

> HSET key:value info1 value1 info2 value2

>> Set a hash mao

>>> HSET player:42 name Hero gold 42 health 100

> HDEL key:value field

>> Delete a field of a hash

> HGET key:value / HGETALL

>> Get value of a hash

> HINCRBY

>> Increase a numeric field

## Lists



