# java-racingcar-precourse

# 기능 요구사항
초간단 자동차 경주 게임을 구현한다. 

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다. 
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차의 이름을 같이 출력한다. 
- 자동차의 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다. 
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다. 
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다. 
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다. 
- 사용자가 잘못된 값을 입력할 경우, IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다. 

## 입력 요구 사항
### 입력

- 경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)
```
pobi,woni,jun
```
- 시도할 횟수
```
5
```
### 출력

- 차수별 실행 결과
```
pobi : --
woni : ----
jun : ---
```
- 단독 우승자 안내 문구
```
최종 우승자 : pobi
```
- 공동 우승자 안내 문구
```
최종 우승자 : pobi, jun
```
### 실행 결과 예시
```
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi : -
woni : 
jun : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----

최종 우승자 : pobi, jun
```

# 🗒 구현 기능 목록

1. 사용자 입력 및 처리
- [X] 쉼표로 구분된 경주할 자동차의 이름 입력 받기
  - [x] 쉼표로 구분하여 자동차 저장하기
  - [X] 자동차 이름의 길이가 5자 이하인지 체크하기
  - [X] 유효하지 않을 시 IllegalArgumentException 처리
- [x] 경주 시도 횟수를 입력받기
  - [x] 시도 횟수가 유효한 값인지 확인
  - [x] 유효하지 않을 시 IllegalArgumentException 처리
2. 자동차의 상태를 저장
- [X] 자동차의 이름을 저장
- [X] 자동차의 위치를 저장
3. 자동차 이동
- [x] 무작위 값을 생성하기
- [X] 무작위 값이 4이상일 경우 전진
4. 경주 진행
- [ ] 매 라운드 진행마다 각 자동차의 상태를 출력
5. 우승자 결정
- [ ] 경주가 끝나면 최종 위치를 비교하여 우승자를 결정
- [ ] 우승자가 여럿이면 쉼표를 기준으로 구분하여 우승자를 결정
6. 결과 출력
- [ ] 최종 우승자 출력