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

- 텍스트 강조

  

  

  

  working directory -(git add)-> staging area -(git commit - m 'message(why)')-> repository

수정

# gitignore

https://www.toptal.com/developers/gitignore



clone : 아무 것도 없는 상태에서 레포를 끌어오는 것

pull : 기존에 있는 것에서 레포를 업데이트(?) 하는 것 -> 다른 곳에서 수정한 것을 끌어옴



가정

- 이미 레포지토리에 커밋이 올라가 있다.
- pull, push 하는 권한이 있다.



- 빈 폴더(상위 폴더에 깃이 없어야 함)에 clone 사용
  - `git clone {url}` -> 새로운 폴더를 만듦
  - `git clone {url} .`  -> 현재 폴더에 그대로

- do something and push commit
  - 원격 저장소가 원본 로컬 저장소보다 상위 버전이 됨.
- pull
  - 원본 로컬 저장소에서 원격 저장소의 코밋을 pull 함
    - `git pull`
