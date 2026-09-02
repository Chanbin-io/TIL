# head, tail, split

## 1. head

파일의 처음 부분을 출력할 때 사용한다.

### 기본 사용

```bash
head a
```

- 처음 10줄 출력

```bash
head -n 10 a
```

- 처음 10줄 출력

```bash
head -10 a
```

- 처음 10줄 출력

### `-n` 사용

```bash
head -n +10 a
```

- 처음 10줄 출력

```bash
head -n -5 a
```

- 마지막 5줄을 제외하고 출력

---

## 2. tail

파일의 마지막 부분을 출력할 때 사용한다.

### 기본 사용

```bash
tail b
```

- 마지막 10줄 출력

```bash
tail -n 10 b
```

- 마지막 10줄 출력

```bash
tail -10 b
```

- 마지막 10줄 출력

```bash
tail -n -10 b
```

- 마지막 10줄 출력

### 특정 라인부터 출력

```bash
tail -n +3 b
```

- 3번째 라인부터 끝까지 출력

### 추가로 학습한 명령

```bash
tail -f
```

---

## 3. split

`split` 명령어와 다음 옵션들을 학습했다.

```bash
split
```

### 학습한 옵션

```text
-l
-C
-a
-d
--additional-suffix
--numeric-suffixes
```

---

## 4. 오늘 학습한 핵심 명령어

```bash
head
head -n

tail
tail -n
tail -f

split
```

### 핵심 정리

```text
head : 파일의 처음 부분을 출력
tail : 파일의 마지막 부분을 출력

head -n -5 : 마지막 5줄을 제외하고 출력
tail -n +3 : 3번째 라인부터 끝까지 출력
```