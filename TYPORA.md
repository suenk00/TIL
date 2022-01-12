메모

<h1>TYPORA 사용설명서
markdown #대제목 ##중제목 #6개까지 가능

# 대제목

## 중제목

### 소제목


- 장점

  1.  문법이 직관적이고 쉽다
  2. 관리가 쉬움
  3. 지원 가능한 플랫폼이 다양함

- 단점

  1. 표준이 없다. 제약 없음.
  2. 처음 학습하는 진입비용 발생
  3. HTML 모든 마크업 기능을 대신하지는 못함. 

  - 링크,표 등은 쉽게 만들지만, 모든 기능을 하지는 못함

- 주의사항

  1. 마크다운의 본질은 글에게 역할을 부여하는 것

  2. 정해진 역할에 맞는 문법을 사용해야 한다.

     - 글씨 진하게 ctrl+b
     - 백틱 `

     EX 글씨 크기를 키우고 싶다면 내용에 제목 역할을 부여하면 아니됨.



## 마크다운 문법

-> 만약 heading1으로 변경하고 싶다면? ctrl+1

1. 제목(Heading)
2. h1-h6



## 리스트(목록)

1. 순서가 있는 목록(숫자로 작성)
2. 순서가 없는 목록 -, * 
3. 모두 tab으로 들여쓰기 가능
4. shift+tab으로 들여쓰기 취소 가능
   - 순서가 있는 목록 안에 순서가 있는 목록 생성 가능



## 강조

1. 굵게
   1. 드래그+ctrl+b 
   2. ** 내용 **
   3. __ 내용 __
2. 기울임
   1. 드래그 + ctrl +i
   2. _ 내용 _
   3. * 내용 *
3. 취소선
   1. ~~ 내용 ~~



## 코드 블럭

- 한 줄 코드: `인라인 코드`와 여러줄 코드인 블럭코드로 나눌 수 있음.

1. 인라인코드: 백틱을 사용해서 코드를 감싸줌.`inline code` 

2. 블럭 코드: ```python처럼 백틱을 3번 입력하고 코드의 종류를 작성함.

   ```print("hello")
   print("hello")
   for i in range(10):
   	print(i)
   ```



## 링크

- 젤다 아님
- [[]''표시할 글자'']]  ( ''이동할 주소'' ) 형태로 작성

​		ex [Google](http://google.com)

- 이동하고자 한다면 ctrl+click 필수



## 이미지

- `![대체 텍스트](''이미지 주소'')
  - `대체 텍스트`란, 이미지가 정상적으로 불러와지지 않았을 때 표시되는 문구입니다.
  - 이미지를 드래그앤드롭으로도 입력 가능

### 주의할 점

- 이미지 업로드 오류 방지를 위해 이미지도 함께 복사될 수 있도록 처리해야함
  1. 우선 이미지 업로드 전 저장 필수!!!
  2. 저장될 폴더와 파일을 같이 업로드한다고 생각. 



## 표

- | -> 파이프 라인
- ctrl+t 단축키로 작성
- 행 늘리려면 ctrl+enter



## 구분선

- --- 하이픈 3개


ctrl+/ 걸린 기능 확인 가능
