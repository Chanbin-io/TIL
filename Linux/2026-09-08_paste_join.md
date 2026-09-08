# paste, join

## 1. paste

여러 파일의 내용을 하나로 합칠 때 사용하는 명령어이다.

```bash
paste
```

---

## 2. join

두 파일의 공통 필드를 기준으로 내용을 합칠 때 사용하는 명령어이다.

기본 형식:

```bash
join [옵션]... 파일1 파일2
```

실습 예시:

```bash
join k1 e1
```

공통된 값을 기준으로 두 파일의 내용을 합쳐 출력한다.

---

## 3. join 주요 옵션

### `-a FILENUM`

```bash
join -a 1 k1 e1
```

- 지정한 파일에서 짝이 없는 행도 함께 출력

### `-e EMPTY`

- 누락된 입력 필드를 지정한 값으로 대체

### `-i`, `--ignore-case`

- 필드를 비교할 때 대소문자 차이를 무시

### `-j FIELD`

- 두 파일에서 사용할 공통 필드를 지정
- `-1 FIELD -2 FIELD`와 같은 의미

### `-o FORMAT`

- 출력 형식을 지정

### `-t CHAR`

- 입력과 출력에서 사용할 필드 구분자를 지정

### `-v FILENUM`

- `-a FILENUM`과 비슷하지만 서로 연결된 행은 출력하지 않음

### `-1 FIELD`

- 파일 1에서 연결 기준으로 사용할 필드를 지정

### `-2 FIELD`

- 파일 2에서 연결 기준으로 사용할 필드를 지정

### `--check-order`

- 입력 파일이 올바르게 정렬되어 있는지 확인

---

## 4. field와 record

오늘 다음 용어를 함께 학습했다.

```text
필드(field)   : 열(column)
레코드(record): 행(row)
```

---

## 5. CSV

오늘 `CSV` 형식에 대해서도 함께 학습했다.

```text
CSV
```

---

## 6. 오늘 학습한 핵심 명령어

```text
paste
join

join -a
join -e
join -i
join -j
join -o
join -t
join -v
join -1
join -2
join --check-order
```

## 핵심 정리

```text
paste : 여러 파일의 내용을 하나로 합침
join  : 공통 필드를 기준으로 두 파일을 연결

field  : 열(column)
record : 행(row)
```
