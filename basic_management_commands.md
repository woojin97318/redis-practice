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

- 마지막으로 성공한 스냅샷의 timestamp를 반환

### 8. SHUTDOWN

```
SHUTDOWN [NOSAVE|SAVE]
```

- Redis 서버 종료
- `NOSAVE` : 종료 전에 데이터를 저장하지 않음
- `SAVE` : 종료 전에 데이터를 저장

### 9. CLIENT LIST, CLIENT KILL

```
CLIENT LIST
CLIENT KILL <ip:port>
```

- `CLIENT LIST` : 현재 연결된 모든 클라이언트 정보를 반환
- `CLIENT KILL` : 특정 클라이언트를 종료

### 10. MONITOR

```
MONITER
```

- 모든 Redis 명령어를 실시간으로 모니터링한다.

### 11. AUTH

```
AUTH <password>
```

- Redis 서버에 인증한다.
- Redis 설정에서 `requirepass` 옵션이 설정되어 있는 경우 사용한다.
