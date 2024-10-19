# java-calculator-precourse

## 기능 요구 사항

```
입력한 문자열에서 숫자를 추출하여 더하는 계산기를 구현한다.

쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다.
예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6
앞의 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있다. 커스텀 구분자는 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
예를 들어 "//;\n1;2;3"과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.
```

## 기능 구현 순서
1. 문자열 입력, 결과값 출력
2. 구분자 찾기
3. 구분자를 이용하여 문자열에서 숫자 추출
4. 숫자의 합 계산
5. 잘못된 값을 입력하는 경우 Exception 발생

## 구현에 필요한 기능 목록
1. Input View
   - [X] ```Console API```를 이용하여 문자열 입력 받은 후, 반환  
2. Split Model
   - [ ] 구분자를 이용하여 문자열 분리
3. Calculator Model
   - [ ] 숫자의 합을 계산하여 반환
4. Output View
   - [X] 결과를 요구 사항에 명시된 출력 형식에 맞게 출력
5. Split Controller
   - [ ] Model, View 결합
6. Delimeter Model
   - [X] 구분자 관리
   - [X] 커스텀 구분자를 포함한 경우, 커스텀 구분자를 찾기
   - [X] 커스텀 구분자 셋팅하는 문자 제거 후 반환