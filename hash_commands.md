### 1. HSET

```
HSET <key> <field> <value>
```

- 특정 key에 대한 해시에 field와 value를 설정

### 2. HGET

```
HGET <key> <field>
```

- 특정 key에 대한 해시에서 특정 field의 value 조회

### 3. HMSET, HMGET

```
HMSET <key> <field1> <value1> <field2> <value2> ...
HMGET <key> <field1> <field2> ...
```

- 여러 field-value 쌍을 한번에 저장(HMSET)하거나, 여러 필드에 대응하는 value을 한 번에 조회

### 4. HDEL

```
HDEL <key> <field1> <field2> ...
```

- 특정 key의 해시에서 하나 이상의 field와 그에 해당하는 value를 삭제

### 5. HEXISTS

```
HEXISTS <key> <field>
```

- 특정 key의 해시에서 특정 field가 존재하는지 여부 확인
- 있다면 1, 없다면 0 리턴

### 6. HKEYS, HVALS, HGETALL

```
HKEYS <key>
HVALS <key>
HGETALL <key>
```

- HKEYS : 특정 key의 해시에서 모든 field 조회
- HVALS : 특정 key의 해시에서 모든 value 조회
- HGETALL : 특정 key의 해시에서 모든 field와 value를 조회

### 7. HINCRBY

```
HINCREBY <key> <field> <increment number>
```

- 특정 key의 해시에서 특정 field의 값을 지정된 숫자만큼 증가시킨다.
- 값이 숫자일 경우에만 적용 가능

### 8. HSETNX

```
HSETNX <key> <field> <value>
```

- 특정 key의 해시에서 field가 존재하지 않을 때만 field와 value를 설정

### 9. HSTRLEN

```
HSTRLEN <key> <field>
```

- 특정 key의 해시에서 특정 field에 저장된 value의 길이를 반환

### 10. HDEL

```
HDEL <key> <field1> <field1> ...
```

- 특정 key의 해시에서 하나 이상의 field와 그에 해당하는 value를 삭제
