# regularExpression

##정규 표현식 연습 시작

# 정규표현식(RegExp)

- 문자 검색(search)
- 문자 대체(replace)
- 문자 추출(extract)

## 텍스트 사이트 

https://regexr.com/

```js

//생성자
new RegExp('표현', '옵션')
new RegExp('[a-z]', 'gi')

//리터럴
/표현/옵션
/[a-z]/gi
```

### 리터럴 방식 편하다


```method
메소드      문법                    설명
exec        정규식.문자열           일치하는 하나의 정보(Array)  반환
test        정규식.문자열           일치 여부(boolean) 반환
match       문자열.정규식           일치하는 문자열의 배열 반환
search      문자열.정규식           일치하는 문자열의 인덱스(number) 반환
replace     문자열.정규식           일치하는 문자열 대체 후 문자열 반환
split       문자열.정규식           일치하는 문자열 분할하여 배열로 반환
toString    생성자_정규식.toString()생성자 함수 방식의 정규식을 리터럴 방식의 문자열로 반환

```


## 예제 문자

```js
const str = `
010-1234-5678
the@naver.com
https://www.omdapi.com/?apikey=7035c60c&s=frozen
The quick brown fox jumps over the lazy dog.
abbcccdddd
`
```

##플래그(옵션)
플래그 | 설명
g | 모든 문자 일치(global)
i | 영어 대소문자 구분 X
m | 여러 줄 일치


## 패턴(표현)
패턴 | 설명
--|--
^ab | 줄 시작에 있는 ab와 일치
ab& | 줄 끝에 있는 ab와 일치

. | 임의의 한 문자와 일치 
a&verbar;b | a or b와 일치
ab? | b가 없거나 b와 일치

{3} | 3개 연속 일치
{3,} | 3개 이상 연속 일치
{3,5} | 3개이상 5개 이하, 연속 일치

[abc] | a or b or c
[a-z] | a ~ z 사이 문자 구간에 일치
[A-Z] | A ~ Z 사이 문자 구간에 일치
[0-9] | 0 ~ 9 사이 문자 구간에 일치
[가-힣] | 가 ~ 힣 사이 문자 구간에 일치

\w | 63개 문자 (word, 대소영문 52개 + 숫자 10개 + _)에 일치
\b | 63개 문자에 일치하지 않는 문자 경계(Boundary)
\d | 숫자(Digit)에 일치
\s | 공백 (space Tab 등)에 일치