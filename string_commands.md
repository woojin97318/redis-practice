### 1. SET

```
SET <key> <value>
```
- 특정 key에 value를 저장
- `SET mykey "Hello World"`

### 2. GET

```
GET <key>
```

- 특정 key에 저장된 value 조회
- `GET mykey`

### 3. APPEND

```
APPEND <key> <value>
```

- 기존 key에 value을 추가, key가 없는 경우 새로 생성
- `APPEND mykey " Redis"`

### 4. STRLEN

```
STRLEN <key>
```

- 특정 key에 저장된 value의 길이를 반환
- `STRLEN mykey`

### 5. INCR(increment), DECR(decrement)

```
INCR <key>
DECR <key>
```

- 특정 key에 저장된 값을 1씩 증가 또는 감소 시킨다.
```
SET counter 10
INCR counter
```

### 6. SETEX (SET with EXPIRE)

```
SETEX <key> <seconds> <value>
```

- 특정 key에 value를 저장하고, 지정된 seconds 후에 만료된다.
- `SETEX mykey 3600 "Hello"`

### 7. MSET, MGET

```
MSET <key1> <value1> <key2> <value2> ...
MGET <key1> <key2> ...
```

- 여러 key-value 쌍을 한번에 저장(MSET)하거나, 여러 key에 대응하는 value를 한 번에 조회

### 8. SETNX (SET if Not eXists)

```
SETNX <key> <value>
```

- 특정 key에 value가 없는 경우에만 값을 설정
- `SETNX newkey "inital value"`

### 9. GETSET

```
GETSET <key> <newvalue>
```

- 특정 key에 저장된 현재 값을 가져오고, 동시에 새로운 값을 설정
- `GETSET mykey "new value"`

### 10. DEL

```
DEL <key>
```

- 특정 key와 그에 해당하는 값을 삭제
- `DEL mykey`
