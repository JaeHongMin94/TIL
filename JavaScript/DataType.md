# JavaScript의 데이터 타입 종류

JavaScript에는 7가지의 타입이 존재합니다.

<table>
  <tr>
    <th>구분</th>
    <th>데이터 타입</th>
    <th>설명</th>
  </tr>
  <tr>
    <td rowspan="6">원시타입</td>
    <td align="center">Number</td>
    <td>정수와 실수 구분 없이 하나의 숫자 타입만 존재</td>
  </tr>
  <tr>
    <td align="center">String</td>
    <td>문자열</td>
  </tr>
  <tr>
    <td align="center">Boolean</td>
    <td>참(ture)과 거짓(false)</td>
  </tr>
  <tr>
    <td align="center">undefined</td>
    <td>정의되지않은 값(암묵적으로 할당)</td>
  </tr>
  <tr>
    <td align="center">null</td>
    <td>값이 없음(명시적으로 사용)</td>
  </tr>
  <tr>
    <td align="center">Symbol</td>
    <td>ES6에서 추가된 타입</td>
  </tr>
  <tr>
    <td colspan="2" align="center">객체 타입</td>
    <td>배열, 객체, 함수</td>
  </tr>
</table>

## 숫자(Number) 타입

JavaScript는 동적 언어이므로 정수, 실수로 나뉘지 않고 Number타입 하나만 존재한다.<br>

## 문자열(String) 타입

문자열 타입은 텍스트 데이터를 나타내는 데 사용합니다. 표현법으로는 작은따옴표(''), 끈따옴표(""), 백틱(``)이 존재합니다.

## 논리(Boolean) 타입

논리 타입은 참과 거짓을 나타낼 때 사용합니다.

- False 값
  - false
  - 0
  - ''
  - null
  - undefined
  - NaN

- True 값
  - true
  - 0이 아닌 수
  - '값'
  - {}
  - []
  
## Undefined

Undefined는 정의되지 않은 값입니다. var 키워드로 변수를 선언하고 초기화 하지 않았을 경우 undefined로 초기화됩니다.

## Null

Null은 값이 없다는 것을 의도적으로 명시할 때 사용합니다. HTML 요소를 검색할 수 없는 경우에 null을 반환합니다.

## Symbol

Symbol은 변경 불가능한 원시 타입의 값입니다.<br>
> 자세한 내용은 추후에 업데이트 예정

## 객체 타입

원시 타입을 제외한 모든 값들은 객체 타입입니다.<br>
배열, 객체, 함수등이 있습니다.
