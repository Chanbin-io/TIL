# touch, redirection

## 1. touch

오늘 `touch` 명령어를 학습했다.

강의에서는 파일 시간 정보와 함께 `touch` 명령어를 다뤘다.

```bash
touch
```

---

## 2. 표준 입출력

리눅스에서는 표준 입력, 표준 출력, 표준 에러를 파일 디스크립터 번호로 구분한다.

```text
0 : stdin  - standard input  - 표준 입력
1 : stdout - standard output - 표준 출력
2 : stderr - standard error  - 표준 에러
```

### stdin

```text
stdin
```

- 표준 입력
- 기본적으로 키보드 입력과 연결

### stdout

```text
stdout
```

- 표준 출력
- 기본적으로 화면 출력과 연결

### stderr

```text
stderr
```

- 표준 에러
- 오류 메시지를 출력할 때 사용

> 강의 화면에는 `stdout 2`로 표시되어 있었지만,
> 표준 에러의 정확한 이름은 `stderr`이다.

---

## 3. 파일 디스크립터

파일이나 입출력 대상을 식별하기 위해 사용하는 번호이다.

```text
0 : 표준 입력
1 : 표준 출력
2 : 표준 에러
```

---

## 4. 파일 열기와 닫기

강의에서 다음 용어를 함께 학습했다.

```text
fopen  : open
fclose : close
```

---

## 5. EOF

```text
Ctrl + D : end of file
```

입력의 끝을 나타낼 때 사용한다.

---

## 6. 리다이렉션

명령어의 입력과 출력 흐름을 다른 곳으로 바꿀 때 사용한다.

### `>`

```bash
command > file
```

- 출력 결과를 파일로 보냄
- 기존 파일의 내용을 덮어씀

### `>>`

```bash
command >> file
```

- 출력 결과를 파일의 끝에 추가
- append 방식

### `<`

```bash
command < file
```

- 파일의 내용을 명령어의 입력으로 사용

### `<<`

```bash
command << WORD
```

- here document
- 여러 줄의 입력을 명령어에 전달할 때 사용

---

## 7. 오늘 학습한 핵심 내용

```text
touch

0 : stdin
1 : stdout
2 : stderr

Ctrl + D : EOF

>  : 출력 리다이렉션
>> : 출력 내용을 뒤에 추가
<  : 입력 리다이렉션
<< : here document
```
