## List

- 순서가 있는 문자열 요소들의 집합을 저장하는 데이터 구조
- FIFO(First In First Out) 큐와 비슷한 특성을 가짐
- 스택과 큐의 기능을 모두 지원

### 1. LPUSH

```
LPUSH <key> <value1> <value2> ...
```

- 리스트의 왼쪽에서부터 하나 이상의 값을 추가

### 2. RPUSH

```
RPUSH <key> <value1> <value2> ...
```

- 리스트의 오른쪽부터 하나 이상의 값을 추가

### 3. LPOP

```
LPOP <key>
```

- 리스트의 왼쪽에서 첫 번째 요소를 제거하고 반환

### 4. RPOP

```
RPOP <key>
```

- 리스트의 오른쪽에서 첫 번째 요소를 제거하고 반환

### 5. LINDEX

```
LINDEX <key> <index>
```

- 리스트의 특정 인덱스에 있는 요소를 조회

### 6. LLEN

```
LLEN <key>
```

- 리스트의 길이를 반환

### 7. LRANGE

```
LRANGE <key> <start> <stop>
```

- 리스트의 특정 범위에 있는 요소들을 조회
- `LRANGE <key> 0 -1` -> 리스트의 모든 요소를 조회
- `LRANGE <key> 0 2` -> index 0, 1, 2의 요소를 조회

### 8. LSET

```
LSET <key> <index> <value>
```

- 리스트의 특정 인덱스에 있는 요소를 새로운 값으로 설정

### 9. LREM

```
LREM <key> <count> <value>
```

- 리스트에서 count만큼의 특정 값을 제거
- count가 0이면 모든 값을 제거

### 10. LTRIM

```
LTRIM <key> <start> <stop>
```

- 리스트의 특정 범위만 남기고 나머지 요소들은 모두 제거

### 11. RPOPLPUSH

```
RPOPLPUSH <source> <destination>
```

- 리스트의 오른쪽에서 요소를 제거하고, 그 요소를 다른 리스트의 왼쪽에 추가

### 12. BLPOP, BRPOP

```
BLPOP <key1> <key2> ... <timeout>
BRPOP <key1> <key2> ... <timeout>
```

- 여러 리스트 중 하나라도 요소를 가지고 있으면 그 요소를 왼쪽(BLPOP) 또는 오른쪽(BRPOP)에서 제거하고 반환
- 만약 모든 리스트가 비어 있으면 timeout동안 블록된다.
