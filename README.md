# java-lotto-precourse


## 프로젝트 개요

- 입력으로 받은 1~45까지의 숫자 범위의 중복되지 않는 로또 번호 6개와 보너스 번호 1개를 맞추기 위한 로또번호를 랜덤하게 생성해주는 간단한 로또 발매기를 구현하는 프로젝트이다. 본 프로젝트는 입력받은 로또번호를 몇 개 맞췄는지 정해진 등수와 상금의 통계를 출력으로 보여주어야 한다.
- 프로젝트 세부 기능 요구 사항
    - 로또 번호의 숫자 범위는 1~45까지이다.
    - 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.
    - 당첨 번호 추첨 시 중복되지 않는 숫자 6개와 보너스 번호 1개를 뽑는다.
    - 당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.
        - 1등: 6개 번호 일치 / 2,000,000,000원
        - 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
        - 3등: 5개 번호 일치 / 1,500,000원
        - 4등: 4개 번호 일치 / 50,000원
        - 5등: 3개 번호 일치 / 5,000원
    - 로또 구입 금액을 입력하면 구입 금액에 해당하는 만큼 로또를 발행해야 한다.
    - 로또 1장의 가격은 1,000원이다.
    - 당첨 번호와 보너스 번호를 입력받는다.
    - 사용자가 구매한 로또 번호와 당첨 번호를 비교하여 당첨 내역 및 수익률을 출력하고 로또 게임을 종료한다.
    - 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.
        - `Exception`이 아닌 `IllegalArgumentException`, `IllegalStateException` 등과 같은 명확한 유형을 처리한다.
        

## 구현할 기능 목록

- 입력 요구 사항 충족
    - 로또 구입 금액, 당첨 번호, 보너스 번호 순으로 입력 받기
    - 로또 구입 금액을 입력 받았을 시에는 금액에 해당하는 개수만큼 랜덤하게 로또번호를 생성하여 출력한다.
- 출력 요구 사항 충족
    - 랜덤으로 생성한 각 로또번호가 몇 개 맞았는지에 대한 당첨 통계를 기능 요구 사항의 당첨 기준과 금액에 따라 출력으로 보여준다.
    - 마지막으로 총 수익률을 계산하여 출력한다.
        - 수익률은 소수점 둘째 자리에서 반올림한다.
- 예외 상황 처리
    - while문을 사용해 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.
        - 각 입력 값의 경우에 대한 잘못된 입력 값은 아래에 적혀있음.


## 입력 요구 사항: 정상적인 경우, 예외 상황 처리

- 로또 구입 금액 입력할 경우
    1. 정상적인 경우
        - 구입 금액 입력 값이 1,000의 배수인 경우
    2. 예외 상황
        - 구입 금액 입력값이 1,000의 배수가 아닌 경우(정수가 아닌 경우도 포함됨)
        - 구입 금액이 양수가 아닌 경우
        - 빈 값이 입력값인 경우
        - 스페이스가 입력값인 경우
- 당첨 번호 입력할 경우
    1. 정상적인 경우
        - 1~45사이의 정수 중 중복되지 않는 6개의 정수가 ‘,’를 기준으로 구분되어 있음.
    2. 예외 상황
        - 1~45범위 밖의 정수인 경우
        - 정수가 중복되는 경우
        - ‘,’가 연속으로 여러개 있는 경우
        - ‘,’가 맨앞과 맨뒤 등 잘못된 위치에 있는 경우
        - ‘,’앞 뒤에 스페이스가 있는 경우
        - 빈 값이 입력값인 경우
        - 스페이스가 입력값인 경우
        - ','말고 다른 구분자가 있는 경우우
- 보너스 번호 입력할 경우
    1. 정상적인 경우
        - 1~45사이의 정수 중 당첨 번호와 중복되지 않는 정수
    2. 예외 상황
        - 1~45범위 밖의 정수인 경우
        - 당첨 번호와 중복되는 경우
        - 빈 값이 입력 값인 경우
        - 스페이스가 입력 값우
        - 입력 값이 숫자가 아닌 경우
        

## 테스트 케이스 작성

- 위의 입력 요구 사항에 대해 테스트 케이스 작성 및 확인
