## 기본 관리 명령어

### 1. FLUSHALL

```
FLUSHALL
```

- 모든 데이터베이스의 모든 key를 삭제
- Redis 인스턴스의 모든 데이터를 초기화

### 2. FLUSHDB

```
FLUSHDB
```

- 현재 선택된 데이터베이스의 모든 키를 삭제

### 3. DBSIZE

```
DBSIZE
```

- 현재 선택된 데이터베이스의 키 개수 반환

### 4. INFO

```
INFO [section]
```

- Redis 서버의 정보를 반환
- `section`을 지정하면 특정 섹션의 정보만 반환

### 5. CONFIG GET, CONFIG SET

```
CONFIG GET <parameter>
CONFIG SET <parameter> <value>
```

- Redis 서버의 설정을 조회하거나 수정

### 6. SAVE, BGSAVE

```
SAVE
BGSAVE
```

- SAVE : (동기 방식) 즉시 스냅샷을 생성하고 데이터를 디스크에 저장
- BGSAVE : (비동기 방식) 백그라운드에서 스냅샷을 생성하고 데이터를 디스크에 저장

### 7. LASTSAVE

```
LASTSAVE
```

- 마지막으로 스냅샷을 생성한 시간을 timestamp 형식으로 반환

### 8. 

```

```

- 
