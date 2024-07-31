## Consistent Hashing

### Background
Hashing is an important concept to partition data in order to achieve scalability. Consistent hashing is widely used in most of the systems for data partition. In this article, lets explore some of the commonly used hashing algorithms also how consistent hashing works.

Lets say we have 4 servers and we want to partition the data among these. A common approach is to use modulo hash function

[key0, key1, key2, key3, key4, key5, key6, key7]

slot = hash(key) % 4

Lets assume that the following is the mapping of keys to the server
server1 = key0, key1
server2 = key2, key3
server3 = key4, key5
server4 = key6, key7

This is all good. Now lets consider the situation of adding/deleting a server to handle the scale.
This warrants a reshuffling of most keys. In case of consistent hashing adding or removing a node will impact only certain keys.

### How consistent hashing works

### Hotspot problem

### Code

### Conclusion