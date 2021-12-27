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


- i 대문자 소문자를 구분 X
- g 

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

