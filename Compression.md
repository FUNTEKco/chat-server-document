IMKit Chat Server v2.0.0 provides compressed response if the client fills Accept-Encoding in request header.

```
Accept-Encoding: gzip
Accept-Encoding: compress
Accept-Encoding: deflate
Accept-Encoding: br
Accept-Encoding: identity
Accept-Encoding: *

// Multiple algorithms, weighted with the quality value syntax:
Accept-Encoding: deflate, gzip;q=1.0, *;q=0.5
```

## Benchmark

| Non-Compressed | Compressed | Ratio |
| -------------- | ---------- | ----- |
| 173209 Bytes   | 17893 Bytes | 10.3% |

NonCompressed
```
curl -so /dev/null "http://triptime.io:3100/rooms" \
     -H "CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=" \
     -H "Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VySWQiOiI1OTA3OGM1ODQ1ZDMwMTYyYWI1NmVkNjAiLCJlbWFpbCI6ImRAZC5jb20ifQ.JjNkjyEkGi8UbD6aJaKUT3PtFF-lu0HfSimiKngMKzE" \
     -H "Content-Type: application/x-www-form-urlencoded; charset=utf-8" \
     -w '%{size_download}'
173209
```

Compressed
```
curl -so /dev/null "http://triptime.io:3100/rooms" \
     -H "Accept-Encoding: gzip" \
     -H "CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=" \
     -H "Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VySWQiOiI1OTA3OGM1ODQ1ZDMwMTYyYWI1NmVkNjAiLCJlbWFpbCI6ImRAZC5jb20ifQ.JjNkjyEkGi8UbD6aJaKUT3PtFF-lu0HfSimiKngMKzE" \
     -H "Content-Type: application/x-www-form-urlencoded; charset=utf-8" \
     -w '%{size_download}'
17893
```

For more information about HTTP Accept-Encoding, please refer to [Accept-Encoding](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Encoding)

