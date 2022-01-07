## 1월 3일 OPR

파이썬 -> 리눅스 추천(윈도우에서는 한계가 분명하다-> 개발자들이 리눅스를 사용했기 때문에 라이브러리에 있어서 문제가 생기는 경우가 있다 //drive.google.com -> my drive -> +버튼 클릭 -> Colaboratory

conda create -n(이름) basic python=3.8(파이썬 버전)        conda activate basic

conda deactivate   conda env list     conda env reomove -n basic

-자료형

숫자형 - (문자들의 집합)정수형 실수형 8진수와 16진수 사칙연산 제곱 나머지 몫

문자열 - (문자들의 집합)이스케이프 코드 연산 인덱싱과 슬라이싱 포맷팅

리스트 - (변수들의 모음)인덱싱과 슬라이싱 연산, 튜플 - (변경할 수 없는 리스트)인덱싱과 슬라이싱 연산  

딕셔너리 - (Key-value pair)추가 삭제, 집합 - (중복x 순서x)교집합 합집합 차집합

-사칙연산 + - * / , **(제곱) %(나머지) //(몫을 정수로)

-문자열 자료형

문자열 만들기

​       큰따옴표 ex)"Hello World", 작은 따옴표 ex)'Python is fun'

​       큰따옴표 3개 연속 ex)"""Life is too short, You need python""", 작은따옴표 3개 연속 ex)'''Life is too short, You need python'''

​       여러 줄을 한 번에 받거나 어퍼스트로피s, 인용문을 쓸 때 사용\'를 사용할 수도 있음

​       이스케이프 코드 -> 미리 정의해둔 문자 조합 // syntaxError -> 문법 오류

문자열 연산하기

​       '+' 문자열 연결하기 '*' 문자열 곱하기 문자열 길이 구하기(len(str)) 

문자열 인덱싱

​       a = "Life is too short, You need Python" a[0] = 'L' a[5] = 'i' a[-1] = 'n' //인덱스는 위치 0부터 시작

문자열 슬라이싱

​       b = a[0] + a{1] + a[2] + a[4] a[0:4] -> 'Life' 마지막 a[4]는 나오지 않는다

​       a[19:] a[19]부터 끝까지 a[:17] a[0]부터 a[16]까지 a[:] 모든 문자열

​       a = 'Pithon' a[1] = 'y' -> 오류 발생(큐플, 뒤에서 설명) 직접적으로 바꿀 수 없음 따라서 a[:1] + 'y' + a[2:] 으로 해줘야함

문자열 포맷팅

​       숫자 대입 %d ex)' I ate %d apples.' % 3 -> 'I ate 3 apples.' //d->decimal

​       문자열 대입 %s

​       변수로 대입 ex) number = 3 "I ate %d apples." % number

​       2개 이상의 변수 대입

​              number = 10 day = "three"

​              "I ate %d apples. so I was sick for %s days." % (number, day)

포맷 코드와 숫자 함께 사용하기

​       정렬과 공백 "%10s" % "hi" -> '    hi'

​                "%-10sjane." % 'hi' -> 'hi    jane.'

​       소수점 표현하기 "%0.4f" % 3.42134234 -> '3.4213'  "%10.4f" % 3.42134234 -> '  3.4213' 총 10지리 소수점 아래 네번째 자리



## 1월 4일 OPR

2022-01-04 2일차 교육 OPR

\1. 문자열

\1) 포맷 코드와 숫자 함께 사용하기

1-1) 숫자/문자열/변수 바로 대입하기

Ex)"I ate {인덱스} apples.".format(숫자/문자열/변수) *숫자 입력 시 문자열로 자동형변환

1-2) 이름으로 넣기

Ex)"I ate {number} apples. so I was sick for {day} days.".format(number = 10, day = 3)

1-3) 정렬 : "{0:[공백을 채울 문자][정렬방향][자리 수]}".format(str) (왼쪽:<, 오른쪽:>, 가운데:^)

1-4) 소수점 표현하기 : “{0:[전체 자리 수].[소수점 아래 자리 수]f”.format(실수)

1-5) {{ 또는 }} 문자 표현하기 : "{{ and }}".format()

\2) f-formating

2-1) f 문자열 포매팅

Ex) f"나의 이름은 {name}입니다. 내년에 제 나이는 {age + 1}입니다."

2-2) 정렬 : 인덱스/값]:[공백을 채울 문자][정렬방향][자리 수]}

\3) 문자열 함수(함수 -> 입력 값을 입력하면 출력 값을 리턴)    

| **함수** | **설명**                                                     | **함수**        | **설명**                                                     |
| -------- | ------------------------------------------------------------ | --------------- | ------------------------------------------------------------ |
| Count()  | 개수를 리턴하는 함수  a.count(‘a’)                           | Upper()/lower() | Upper() : 대문자로 바꾸어 리턴  Lower() : 소문자로 바꾸어 리턴 |
| Find()   | 인덱스를 리턴하는 함수  a.find(‘a’) *a가 없을 때 -1 리턴     | Strip()         | 공백을 제거하여 리턴하는  함수  Rstirp(오른쪽만), Lstrip(왼쪽만) |
| Index()  | 인덱스를 리턴하는 함수  a.index(‘a’) *a가 없을 때 오류       | Replace()       | 변수 내의 문자열을 다른  문자열로 변환하여 리턴하는 함수  a.replace(str1, str2) |
| Join()   | 문자열 사이에 다른 문자를  삽입하여 리턴하는 함수  ‘.’.join(‘abc’) -> ‘a.b.c’ | Split()         | 문자열을 잘라서 리턴하는  함수  a.split(자르는 위치(디폴트 공백)) |

\2. 리스트

1)리스트 만들기

1-1) 대괄호 사용, List 객체 만들기 *리스트 내에 리스트를 넣음으로 고차원 만들 수 있음





# Markdown?

### 1. 헤딩(Heading)

- 문서의 제목이나 소제목

 - #의 개수에 따라 제목의 수준을 구별(h1 ~ h6)
 - 문서 구조의 기본
 - 글자 크기를 키우기 위해서 사용x

### 2. 리스트(List)

- 순서가 있는 리스트와 순서가 없는 리스트
- 목록을 표시하기 위해 사용
- 많이 사용하는 태그 중 하나
- `1. ` : 순서가 있는 리스트 생성
- `- / *` : 순서가 없는 리스트 생성
- tab키를 이용해서 들여쓰기 가능

### 3. 코드 블럭(Code Block)

- 일반 텍스트와 다르게 코드를 이쁘게 출력

- 개발자가 마크다운을 사랑하는 이유 중 하나

- 사용하는 프로그램에 따라 특정 언어를 명시하면 구문 강조(Syntax Highlighting)

- ` ``` ` : 코드 블럭(python, java, c, c++ 등 모두 가능)

- ```python
  print(input())
  ```

### 4. 링크(Link) ` [string](url) `

- string은 보여지는 부분, url은 연결할 곳

- 다른 페이지로 이동하는 링크를 삽입

- 필요하다면 파일의 경로를 넣어 다운로드 가능한 링크로 만들 수 있다.

- http 잊지 않기(full link)

  

### 5. 텍스트 강조(Text Emphasis)

- 기울임 : `*텍스트*`혹은 `_글자_`
- 굵게 : `**텍스트**` 혹은 `__글자`
- 취소선 : `~~글자~~`
- 함께도 사용 가능



### 6. 이미지(Image) `![대체 텍스트](url)`

- 이미지 삽입 가능
- 대체 텍스트 -> 이미지 정상적으로 불러오지 못했을 때 표시되는 문구



### 7. 인용(Blockquote)

- 주석이나 인용 문구 표현
- `>`를 사용, 갯수에 따라 중첩이 가능

> 인용문을 작성합니다.
>
> > 중첩된 인용문1
> >
> > > 중첩된 인용문2
> > >
> > > > 중첩된 인용문3
> > > >
> > > > > 중첩된 인용문4



### 8. 표(Table)

- 테이블(표)를 생성
- `파이프(|)`와 `하이폰(-)`을 이용해서 행과 열 구분
- 테이블 양쪽 끝의 `파이프(|)`는 생략 가능
- 헤더 셀을 구분할 때는 `3개 이상의 하이폰(-)`이 필요함
- Typora 에서는 `ctrl + T`를 통해서 쉽게 표 생성 가능
- 행을 늘릴 때 `ctrl + T`



### 9. 수평선(Horizontal Rule)

- 구분 선 생성
- `- * _`을 3번 이상 연속으로 작성



## 10. 목차

- (`#가고자 하는 이름)` 쓰면 원하는 제목으로 이동 가능
- 웹페이지에 이용

[1. 개발을 하고 싶어요](#개발을-하고-싶어요)



## 개발을 하고 싶어요

working directory -(git add)-> staging area -(git commit - m 'message(why)')-> commit area -(git push)-> repository

# **Git**

---

## 한 번만 해도 되는 작업

- `git config --global user.name [github_username]` : username 등록
- `git config --global user.name` : username 확인
- `git config --global user.email <github_email> ` : email 등록

- `git config --global user.email ` : email 확인

---

- `git init` : git 시작
- `git add`
  - `git add .` : 모든 파일 staging area에 올리기
  - `git add [file_name]`: 파일 staging area에 올리기 
- `git commit -m 'commit_message'`
- `git remote add origin [git_repository_url]` : repository 연결
- `git push origin master` : github로 밀어내기
  - `git push -u origin master`: 다음 push 때는 origin master 안 적어도 됨



#### gitignore

https://www.toptal.com/developers/gitignore



- clone : 아무 것도 없는 상태에서 레포를 끌어오는 것

- pull : 기존에 있는 것에서 레포를 업데이트(?) 하는 것 -> 다른 곳에서 수정한 것을 끌어옴



#### 가정

- 이미 레포지토리에 커밋이 올라가 있다.
- pull, push 하는 권한이 있다.

---

- 빈 폴더(상위 폴더에 깃이 없어야 함)에 clone 사용
  - `git clone {url}` -> 새로운 폴더를 만듦
  - `git clone {url} .`  -> 현재 폴더에 그대로

- do something and push commit
  - 원격 저장소가 원본 로컬 저장소보다 상위 버전이 됨.
- pull
  - 원본 로컬 저장소에서 원격 저장소의 commit을 pull 함
    - `git pull`





#### branch

- `git branch [branch_name]` : 새로운 branch 생성
- `git branch` : branch 확인
- `git merge [branch_name]` : branch와 합침 -> 기준이 될 branch에서
- `git branch -d [branch_name]` : branch 삭제
- `git switch [branch_name]` : branch 이동
  - `git switch -c 'branch_name'`: branch 생성 후 이동
  - `git checkout` : 과거에 사용했었음



- `git log`

  - ` --oneline` : 한 줄로

  - `--all` : 모든 branch의 log 확인 가능 

  - `--graph` : branch의 방향을 눈으로 확인하기 쉬움

    ![image-20220107103212689](README/image-20220107103212689.png)

  - --(개수) : 최근 개수의 log만





- git merge 이후 conflict 생겼을 때 conflict 해결 후 git commit 자동으로 merge branch [합친 branch_name]이라는 메세지 생성
  - Fast-foward 메세지 : 잘 합쳐짐



#### store

- `git restore [file_name]`
  - 다시는 다시 되돌릴 수 없다 -> 신중하게
  - `git add` 전 : commit했던 상태로 복구
  - `git add` 후 : staging area에 있기 때문에 변하지 않음
  - `git restore --staged [file_name]` : commit에 있는 수정 전의 파일로 working directory 내의 파일을 복구함

- `git rm --cached [file_name]` : untracked 상태로 바꿔준다
- `git commit --amend` 
  - 파일 수정이 없으면 commit 메세지만 재작성
  - 파일 수정이 있으면 그것을 반영하여 commit을 덮어씌운다

- `git diff` : working directory <-> staging area or commits 비교(add x)
  - `git diff --staged` : staging area <-> commits 비교(add o)

- `git reset`

  - `--hard` : working directory, staging area, commits 모두 지워진 상태
  - `--mixed` : add, commit 하면 원래 상태로 돌아올 수 있다(untracked 상태로 존재)
  - `--soft` : commit만 하면 원래 상태로 돌아올 수 있다(add 되어있는 상태로 존재)
  - `git reflog` : reset한 것까지 확인가능한 log

- `git revert` : revert를 했다는 commit을 남기며(log 남음) 원하는 commit을 지울 수 있다

  - `git revert`한 후에 `git reset`으로 다른 commit으로 넘어가면 다시 살릴 수 있다

    -> revert 한 것을 다시 revert 가능

  - `git revert [commit_id1]..[commit_id2]` : id1 **'뒤'**부터 id2까지 revert
  - 가정
    - a, b, c, d, e까지 했는데 d는 지우고 싶고 e는 살리고자 할 때 사용



#### github 꾸미기

https://startbootstrap.com/

(user_name).github.io/(repo_name)
