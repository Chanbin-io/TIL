# ls, dir, vdir, dircolors

## 1. ls

디렉터리의 내용을 확인할 때 사용하는 명령어이다.

```bash
ls
```

---

## 2. ls 주요 옵션

### `-a`

```bash
ls -a
```

- 모든 파일을 표시

### `-A`

```bash
ls -A
```

- `.` 과 `..` 을 제외하고 모든 파일을 표시

### `-l`

```bash
ls -l
```

- 파일의 자세한 정보를 표시

### `-h`

```bash
ls -h
```

- 크기를 사람이 읽기 쉬운 형태로 표시

### `-F`

```bash
ls -F
```

- 파일의 특성을 표시
- 예: `*`, `/`, `=`, `>`, `@`, `|`

### `-i`

```bash
ls -i
```

- inode 정보를 표시

### `-R`

```bash
ls -R
```

- 하위 디렉터리까지 재귀적으로 표시

---

## 3. 정렬 관련 옵션

### `-S`

```bash
ls -S
```

- 파일 크기를 기준으로 정렬

### `-r`

```bash
ls -r
```

- 정렬 순서를 반대로 표시

### `-t`

```bash
ls -t
```

- 시간 정보를 기준으로 정렬

---

## 4. 시간 정보

학습한 시간 정보는 다음과 같다.

```text
-t : modification time
-u : access time
-c : change time
```

### 의미

```text
Access : 접근
Modify : 수정
Change : 속성 변경
```

---

## 5. dir, vdir, dircolors

오늘 다음 명령어들도 함께 학습했다.

```bash
dir
vdir
dircolors
```

---

## 6. 오늘 학습한 핵심 명령어

```text
ls
ls -a
ls -A
ls -l
ls -h
ls -F
ls -i
ls -R
ls -S
ls -r
ls -t
ls -u
ls -c

dir
vdir
dircolors
```

## 핵심 정리

```text
-a : 모든 파일 표시
-A : . 과 .. 을 제외하고 모든 파일 표시
-l : 자세한 정보 표시
-h : 사람이 읽기 쉬운 크기로 표시
-F : 파일 특성 표시
-i : inode 표시
-R : 하위 디렉터리까지 재귀적으로 표시

-S : 크기 기준 정렬
-r : 역순 정렬
-t : 시간 기준 정렬

Access : 접근
Modify : 수정
Change : 속성 변경
```
