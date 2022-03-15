# 04 Delay 와 Rollback

## Deterministic

- 두 사용자 간 상태가 Latency 로 인해 Sync 깨진 Desync 상태 방지해야 한다

### Delay

- Latency 시간만큼 delay 를 만들어 sync를 맞춘다
- 하지만 지연 시간이 있기에 느려지는 단점이 있다

### Rollback

- 상대방 입력이 들어온 시간에서 Latency를 뺀 시간 으로 되돌아가 입력들을 처리하는 과정을 가진다
- Rollback 된 사용자는 불공정함을 느끼고 게임이 렉이 걸리거나 튄 걸로 판단하는 문제가 있다
- 구현이 굉장히 어렵다 -> 뒤감기, 앞감기, 중간에 입력을 집어넣기

### 해결책

- Delay 와 Rollback 을 모두 사용하며 롤백은 부분적으로 사용한다
