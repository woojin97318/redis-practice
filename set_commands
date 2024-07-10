### 1. SADD

```
SADD <key> <member1> <member2> ...
```

- 집합에 하나 이상의 멤버를 추가

### 2. SMEMBERS

```
SMEMBERS <key>
```

- 집합의 모든 멤버 조회

### 3. SREM

```
SREM <key> <member1> <member2> ...
```

- 집합에서 하나 이상의 멤버를 제거

### 4. SISMEMBER

```
SISMEMBER <key> <member>
```

- 특정 멤버가 집합에서 존재하는지 확인
- 존재하면 1, 아니면 0을 반환

### 5. SCARD

```
SCARD <key>
```

- 집합의 멤버 수를 반환

### 6. SPOP

```
SPOP <key> [count]
```

- 집합에서 하나 이상의 임의읭 멤버를 제거하고 반환
- count가 지정되지 않으면 한 개의 멤버를 제거하고 반환

### 7. SRANDMEMBER

```
SRANDMEMBER <key> [count]
```

- 집합에서 하나 이상의 임의의 멤버를 반환
- count가 지정되지 않으면 한 개의 멤버를 반환

### 8. SMOVE

```
SMOVE <source> <destination> <member>
```

- 한 집합에서 다른 집합으로 멤버를 이동

### 9. SDIFF, SINTER, SUNION

```
SDIFF <key1> <key2> ...
SINTER <key1> <key2> ...
SUNION <key1> <key2> ...
```

- SDIFF : 첫 번째 집합에서 다른 집합과의 차집합을 반환
- SINTER : 집합 간의 교집합을 반환
- SUNION : 집합 간의 합집합을 반환

### 10. SDIFFSTORE, SINTERSTORE, SUNIONSTORE

```
SDIFFSTORE <destination> <key1> <key2> ...
SINTERSTORE <destination> <key1> <key2> ...
SUNIONSTORE <destination> <key1> <key2> ...
```

- 집합 연산 결과를 다른 집합에 저장
