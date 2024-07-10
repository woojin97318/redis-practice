## Sorted Set

- 각 멤버에 대해 연결된 점수(score)가 있는 정렬된 집합을 저장하는 데이터 구조
- Sorted Set은 멤버들을 유일하게 식별하고, 각 멤버는 정렬 기준인 점수와 함께 저장
- score는 점수이며 이 점수를 기준으로 정렬

### 1. ZADD

```
ZADD <key> <score1> <member1> <score2> <member2> ...
```

- 정렬된 집합에 멤버와 점수를 추가

### 2. ZRANGE

```
ZRANGE <key> <start> <stop> [WITHSCORES]
```

- 정렬된 집합에서 범위 내의 멤버들을 조회
- start부터 stop까지의 인덱스를 기준으로 조회 (인덱스는 0부터 시작)
- WITHSCORES 옵션을 추가하면 멤버와 점수를 함께 반환

### 3. ZREVRANGE

```
ZREVRANGE <key> <start> <stop> [WITHSCORES]
```

- 정렬된 집합에서 역순으로 범위 내의 멤버들을 조회
- start부터 stop까지의 역순 인덱스를 기준으로 조회
- WITHSCORES 옵션을 추가하면 멤버와 점수를 함께 반환

### 4. ZRANK, ZREVRANK

```
ZRANK <key> <member>
ZREVRANK <key> <member>
```

- 정렬된 집합에서 멤버의 순위(인덱스)를 조회 (score가 아니라 index를 조회)
- ZRANK : 작은 순서(ASC)로 순위를 반환
- ZREVRANK : 큰 순서(DESC)로 순위를 반환

### 5. ZSCORE

```
ZSCORE <key> <member>
```

- 정렬된 집합에서 특정 멤버의 점수를 조회

### 6. ZREM

```
ZREM <key> <member1> <member2> ...
```

- 정렬된 집합에서 하나 이상의 멤버를 제거

### 7. ZCOUNT

```
ZCOUNT <key> <min_score> <max_score>
```

- 정렬된 집합에서 주어진 점수 범위 내의 멤버 수를 반환
- min부터 max까지의 점수 점위를 조회

### 8. ZINCRBY

```
ZINCRBY <key> <increment> <member>
```

- 정렬된 집합에서 특정 멤버의 점수를 증가시킨다.
- increment는 증가할 양을 나타낸다.

### 9. ZCARD

```
ZCARD <key>
```

- 정렬된 집합의 멤버 수를 반환

### 10. ZLEXCOUNT

```
ZLEXCOUNT <key> <min_score> <max_score>
```

- 정렬된 집합에서 사전 순서 범위 내의 멤버 수를 반환

1. 정렬된 집합 생성 및 변수 추가
  - 모든 멤버의 점수를 0으로 설정하여 사전 순서 비교가 이루어지도록 함

```
ZADD myzset 0 "apple"
ZADD myzset 0 "banana"
ZADD myzset 0 "cherry"
ZADD myzset 0 "date"
ZADD myzset 0 "elderberry"
```

2. 사전 순서 범위 내의 멤버 수 조회

```
> ZLEXCOUNT myzset [b [d
> 3
```

3. 범위 예시

- `ZLEXCOUNT myzset [b [d` : "banana," "cherry", "date"를 포함
- `ZLEXCOUNT myzset (b (d` : banana와 "date를 제외하고 "cherry"만 포함
- `ZLEXCOUNT myzset [b (d` : banana와 "cherry"를 포함하고 "date"를 제외
- `ZLEXCOUNT myzset (b [d` : banana를 제외하고 "cherry"와 "date"를 포함

### 11. ZREMRANGEBYRANK, ZREMRANGEBYSCORE, ZREMRANGEBYLEX

```
ZREMRANGEBYRANK <key> <start> <stop>
ZREMRANGEBYSCORE <key> <min> <max>
ZREMRANGEBYLEX <key> <min> <max>
```

- 정렬된 집합에서 순위, 점수, 사전 순서에 따라 멤버를 범위로 제거
