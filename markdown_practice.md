# 마크다운
##제목
`#+space` h1~h6
```
# 제목1
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6
```

## 목록
순서가 없는 목록 : -, *, + 띄어쓰기 후 작성
- 목록
* 목록작성
  + 목록
    - 목록 여기는 탭으로 들여쓰기

순서가 있는 목록 : 1. 2. 3.

1. 목록
2. 이어서
3. 목록이
4. 만들어
   1. 들여쓰기도
   2. 가능합니다.
5. 집니다.

## 문자 서식
굵게, 기울임, 취소선

**굵게**  2칸스페이스  
 __굵게__ ctrl+b  
*기울임*, _기울임_ *드래그하고 별하나*  
~~취소~~

## 코드
인라인 코드 : 문장 중간에 코드를 삽입하고 싶을 때

> 예시
파이썬에서 문장을 출력하고 싶을 때, 사용하는 함수는 `print` 입니다.

블럭 코드 : 코드에 언어를 선택하여, syntax highlight를 넣을 수 있다.

```python
for i in range(10):
    print(i)
```

```bash
touch a.txtx
mv a. txt hello
```

## 링크
`[표시] (url)`

[LMS](https://learn.dailyalgo.kr/courses/%EB%B9%84%EC%A6%88%EB%8B%88%EC%8A%A4-%EB%AC%B8%EC%A0%9C-%ED%95%B4%EA%B2%B0%EC%9D%84-%EC%9C%84%ED%95%9C-%EC%8B%A4%EB%AC%B4%ED%98%95-ai%EB%8D%B0%EC%9D%B4%ED%84%B0%EB%B6%84%EC%84%9D-%EA%B3%BC%EC%A0%95-2%EA%B8%B0/2cb611ac-3a00-8020-a77b-d090810155dd#2cb611ac3a008095bdc0f94fabaa4303)


## 이미지
![git logo](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/1024px-Git-logo.svg.png)

## 표
|동물|종류|다리수|
|---|---|---|
|사자|포유류|4개
|닭|조류|2개|


# TIL Day 01
>2025년 12월 17일

## Why Git & Github?
![Git logo](https://user-images.githubusercontent.com/49775540/168756716-68f9aebb-380f-4897-8141-78d8403f6113.png)

## Git
* 분산 버전 관리 프로그램
* 백업, 복구, 협업을 위해 사용
* [Git 공식문서](https://git-scm.com/book/ko/v2)

## Github
* Git을 사용하는 프로젝트의 협업을 위한 웹호스팅 서비스
* 포트폴리오를 자랑할 수 있는 공간
* *1일 1커밋 하기*
* [이동욱님 Github 계정](https://github.com/jojoldu)

## CLI
> **CLI** (Command Line Interface, 커맨드 라인 인터페이스)는 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식을 뜻한다.

### 터미널 명령어 정리

| 명령어 |              설명               |
| :----: | :-----------------------------: |
| mkdir  |            폴더 생성            |
| touch  |            파일 생성            |
|   ls   |   현재 폴더의 파일 목록 출력    |
|   cd   |        다른 폴더로 이동         |
|   rm   | 파일 삭제 / 폴더 삭제 (-r 옵션) |


```
예시

$ mkdir test

$ touch a.txt

$ ls
$ ls -a

$ cd ..
$ cd test

$ rm a.txt
$ rm -r test
```

## Visual Studio Code
>**Visual Studio Code** (비주얼 스튜디오 코드)는 마이크로소프트에서 개발한 텍스트 에디터의 한 종류이다.

### 장점
* Windows, Mac, Linux 운영체제를 모두 지원한다.
* 기존 개발 도구보다 빠르고 가볍다.
* Extension을 통해 다양한 기능을 설치할 수 있어서, 무한한 확장성을 가진다.
* 무료로 사용 가능하다.

### Git Bash 연동하기
1. 터미널을 연다. (Ctrl + ` )
2. 화살표를 누르고 *Select Default Profile*을 클릭한다.
3. Git Bash를 선택한다.
4. 휴지통을 눌러서 터미널을 종료하고, 재시작한다.
    - 휴지통은 Kill Terminal 로써, 터미널 자체를 아예 종료한다.
    - 닫기는 Close Terminal 로써, 터미널을 종료하지 않고 창만 보이지 않게 만든다.
5. 기본 터미널이 Git Bash로 열리는지 확인한다.

## Markdown
  > **Markdown** (마크다운)은 일반 텍스트 기반의 경량 Markup (마크업) 언어이다.

### Markup (마크업) 이란?
- 마크(Mark)로 둘러싸인 언어를 뜻한다. 마크란 글의 역할을 지정하는 표시이다.
- HTML도 마크업 언어인데, 글에 제목의 역할을 부여할 때 `<h1>제목1</h1>` 과 같이 작성한다.

### 마크다운의 장점과 단점
1. 장점
   * 문법이 직관적이고 쉽다.
   * 지원 가능한 플랫폼과 프로그램이 다양하다.
  
2. 단점
   * 표준이 없어서 사용자마다 문법이 상이하다.
   * 모든 HTML의 기능을 대신하지는 못한다.

#### 주의사항
* 마크다운의 본질은 글에 **역할**을 부여하는 것이다.
* 반드시 역할에 맞는 마크다운 문법을 작성한다. 글씨를 키우고 싶다고 해서 본문에 제목의 역할을 부여하면 안된다.

#### 참고자료
* [Markdown Guide](https://www.markdownguide.org/basic-syntax/)  
* [마크다운 문법 정리](https://gist.github.com/ihoneymon/652be052a0727ad59601)