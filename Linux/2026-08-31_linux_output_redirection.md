# Linux 파일 출력과 리다이렉션

## 1. 실습 환경

WSL Ubuntu에서 실습하였다.

처음에는 Windows의 System32 경로에서 실습하고 있었다.

```bash
/mnt/c/Windows/System32/d3
```

Linux 홈 디렉터리로 이동하였다.

```bash
cd ~
pwd
```

결과:

```text
/home/chanbin
```

실습용 디렉터리를 생성하였다.

```bash
mkdir -p linux-study/d3
cd linux-study/d3
pwd
```

결과:

```text
/home/chanbin/linux-study/d3
```

### mkdir -p

```bash
mkdir -p linux-study/d3
```

`-p` 옵션을 사용하면 중간 디렉터리가 존재하지 않아도 필요한 디렉터리를 함께 생성할 수 있다.

---

## 2. cat

`cat`은 파일의 내용을 터미널에 출력할 때 사용한다.

```bash
cat a1
```

여러 파일을 한 번에 출력할 수도 있다.

```bash
cat a1 a2
```

### 주요 옵션

```bash
cat -n a1
```

- `-n` : 모든 행에 행 번호를 표시

```bash
cat -b a1
```

- `-b` : 공백 라인을 제외하고 행 번호를 표시

---

## 3. 출력 리다이렉션

### `>`

명령어의 출력 결과를 파일에 저장한다.

```bash
cal > a1
```

기존 파일이 존재하면 기존 내용을 덮어쓴다.

예시:

```bash
hostname > a5
cal > a5
```

두 번째 명령을 실행하면 기존 `hostname` 결과는 사라지고 `cal` 결과로 변경된다.

### `>>`

기존 파일의 내용을 유지하면서 마지막에 새로운 내용을 추가한다.

```bash
cal > a5
hostname >> a5
```

정리:

```text
>   기존 내용을 덮어쓰고 저장
>>  기존 내용 뒤에 추가
```

---

## 4. cat으로 파일 합치기

두 파일의 내용을 연결해서 출력할 수 있다.

```bash
cat a1 a2
```

결과를 새로운 파일에 저장할 수도 있다.

```bash
cat a1 a2 > a3
```

순서를 변경하면 저장되는 내용의 순서도 달라진다.

```bash
cat a2 a1 > a4
```

---

## 5. cat으로 직접 파일 만들기

```bash
cat > a7
```

이후 내용을 직접 입력하였다.

```text
aa
bb
cc
dd
ee
```

입력 종료 후 확인:

```bash
cat a7
```

파일명을 지정하지 않고 `cat`만 실행하면 표준 입력을 기다린다.

```bash
cat
```

입력한 내용이 그대로 다시 출력된다.

---

## 6. tac

`tac`은 파일 내용을 `cat`과 반대 순서로 출력한다.

```bash
tac a5
```

파일의 마지막 줄부터 첫 번째 줄까지 역순으로 표시된다.

출력 결과를 새로운 파일에 저장할 수도 있다.

```bash
tac a5 > a6
```

---

## 7. tee

`tee`는 명령어의 출력 내용을 화면에 보여주면서 파일에도 기록할 때 사용할 수 있다.

### `tee -a`

```bash
tee -a
```

- `-a` : 기존 파일의 마지막에 내용을 추가한다.

---

## 8. nl

`nl`은 파일 내용에 행 번호를 붙여 출력할 때 사용한다.

학습 내용에서는 다음과 같이 정리하였다.

```text
nl ≒ cat -b
```

공백 라인을 제외하고 행 번호를 붙이는 방식과 유사하다.

강의에서 함께 다룬 옵션:

```text
-i10
-v100
-l1000
-w10
```

---

## 9. 사용자 및 시스템 정보 확인

### who

```bash
who
```

현재 로그인 세션 정보를 확인한다.

WSL 환경에서는 출력이 나타나지 않았다.

### whoami

```bash
whoami
```

결과:

```text
chanbin
```

현재 명령어를 실행 중인 사용자 계정을 확인할 수 있다.

파일에 저장:

```bash
whoami > a2
```

### hostname

```bash
hostname
```

결과:

```text
DESKTOP-BG7BQBG
```

현재 시스템의 호스트 이름을 확인한다.

---

## 10. 오늘 학습한 핵심 명령어

```bash
cd
pwd
mkdir -p

cal
who
whoami
hostname

cat
cat -n
cat -b
tac

tee
tee -a

nl

>
>>
```

### 핵심 정리

```text
cat   : 파일 내용을 출력
tac   : 파일 내용을 역순으로 출력

>     : 출력 결과를 파일에 저장하며 기존 내용은 덮어씀
>>    : 기존 파일 마지막에 내용을 추가

tee   : 출력 내용을 화면과 파일에 함께 전달
tee -a: 기존 파일 뒤에 추가

nl    : 파일 내용에 행 번호를 붙여 출력
```
