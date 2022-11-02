# 로또
## 진행 방법
* 로또 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.
## 온라인 코드 리뷰 과정
* [텍스트와 이미지로 살펴보는 온라인 코드 리뷰 과정](https://github.com/next-step/nextstep-docs/tree/master/codereview)


## 1단계 - 문자열 계산기
### 기능 요구사항 
* 사용자가 입력한 문자열 값에 따라 사칙연산을 수행할 수 있는 계산기를 구현해야 한다.
* 입력 문자열의 숫자와 사칙 연산 사이에는 반드시 빈 공백 문자열이 있다고 가정한다.
* 나눗셈의 경우 결과 값을 정수로 떨어지는 값으로 한정한다.
* 문자열 계산기는 사칙연산의 계산 우선순위가 아닌 입력 값에 따라 계산 순서가 결정된다. 즉, 수학에서는 곱셈, 나눗셈이 덧셈, 뺄셈 보다 먼저 계산해야 하지만 이를 무시한다.
* 예를 들어 2 + 3 * 4 / 2와 같은 문자열을 입력할 경우 2 + 3 * 4 / 2 실행 결과인 10을 출력해야 한다.
#### 구현 목록
[x] 덧셈
[x] 뺄셈
[x] 곱셈
[x] 나눗셈
[x] null 또는 공백문자열시 IllegalArgumentException
[x] 사칙연산 기호가 아닌 경우 IllegalArgumentException
[x] 사칙연산을 모두 포함하는 기능 구현


## 2단계 - 로또(자동)
### 기능 요구사항
* 로또 구입 금액을 입력하면 구입 금액에 해당하는 로또를 발급해야 한다.
* 로또 1장의 가격은 1000원이다.
* 당첨번호를 입력하면 생성한 로또 번호들과 대조한다.
* 3개 일치 (5000원),4개 일치 (50000원), 5개 일치 (1500000원), 6개 일치 (2000000000원) 한 로또 개수를 센다
* 수익율을 계산하여 출력한다 (총상금/총지출금)
### 구현목록
[x] 금액에 따라 생성할 로또 개수 계산
[x] 로또 티켓 자동생성
[x] 로또 티켓이 당첨 번호인지 확인 (순위 반환)
[x] 수익율 계산

## 3단계 - 로또(2등)

### 기능 요구사항

* 2등을 위해 추가 번호를 하나 더 추첨한다.
* 당첨 통계에 2등도 추가해야 한다.

### 구현목록

[x] 보너스 번호를 입력받기
[x] 5개 일치하는 로또 중 보너스 번호 일치하면 2등
[x] 신규로 2등(보너스번호일치) 추가하면서, 기존 2~4등을 3~5등이 되도록 수정

## 4단계 - 로또(수동)

### 기능 요구사항

* 현재 로또 생성기는 자동 생성 기능만 제공한다. 사용자가 수동으로 추첨 번호를 입력할 수 있도록 해야 한다.
* 입력한 금액, 자동 생성 숫자, 수동 생성 번호를 입력하도록 해야 한다.

## 구현목록

[ ] 자동/수동 생성할 티켓 갯수 계산
[ ] 수동 개수만큼 입력받은 티켓 생성하기