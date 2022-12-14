# PokerGame
## 7포커 코드 개발                         

#### 개발 중심점
1. 나와 상대에게 각각 __7장의 랜덤 카드__ 부여
2. 코드를 통해 패의 __족보를 알아보기__
3. 서로의 패 비교 후, __승부 결정__
4. 7장의 카드를 매순간 정렬하며 비교하기 때문에 __여러가지 정렬 알고리즘__ 을 사용해보며 비교해봤습니다.


#### 족보 알아보기
1. 패를 랜덤으로 2명에게 7장씩 부여
2. 각각 패를 족보가 높은 순부터 함수의 알고리즘을 따라 패의 종류를 알아보기
<br>a. 패를 내림차순으로 정렬함
<br>b. 처음 '로얄스트레이트플러쉬'부터 패의 족보를 확인
<br>c. 한 단계씩 내려가며 '스트레이트플러쉬' ~ '탑' 확인
<br>d. 해당 족보의 정보를 넘김
<br>d. 두 패의 정보를 비교 (비교 순서: 족보등급 > 카드 숫자 > 카드 모양)

#### 정렬 알고리즘
1. 버블 정렬
2. 선택 정렬
3. 삽입 정렬
4. 병합 정렬

#### 코드 사용법
1. 개발 환경: Google Colab
2. 사용법 각 파트 별로 실험을 해볼 수 있음
<br>a. 각 코드 별 그대로 실행하면 즉석으로 결과 확인 가능
<br>b. 파이썬 문법 기반 타 프로그램으로 실행가능

--------
## 실험

#### 정렬의 방법을 달리하면 계산 속도에 차이가 많이 나는가?
1. 4가지 정렬 알고리즘을 통해 비교
<br>__버블 정렬, 선택 정렬, 삽입 정렬, 병합 정렬__
2. 실험 시 같은 패 사용

Mycard = [("4", 10), ("2",10), ("4",1), ("2",9), ("3",9), ("4",2), ("1",10)]

OpponentCard = [("1", 10), ("3",10), ("4",5), ("1",8), ("3",8), ("4",8), ("2",13)]

#### 실험 예시
![2022-12-04 (2)](https://user-images.githubusercontent.com/83060689/205482615-47bb284a-f7fd-4377-9e78-8f29eafe261b.png)
⬆사진과 같이 함수를 실행 시키고 결과가 나오는 시간 측정

#### 실험 결과
|표|버블 정렬|선택 정렬|삽입 정렬|병합 정렬|
|:---|:---:|:---:|:---:|---:|
|1.|0.17248|0.17509|0.16980|0.16659|
|2.|0.16395|0.16468|0.16180|0.16785|
|3.|0.17103|0.16616|0.16427|0.16967|
|4.|0.16670|0.17103|0.16451|0.17086|
|5.|0.16958|0.16372|0.16813|0.16533|
|평균|0.168748|0.168136|0.165702|0.16806|


#### 결과 분석
평균 시간을 비교해보니 큰 차이가 나질 않음

카드 정렬을 사용하는 횟수는 여러차례 있으나

결과적으로 7장 밖에 비교를 안하기 때문에

시간에서 큰 차이가 없는 결과를 보임

<br>
유튜브 영상 링크

https://www.youtube.com/watch?v=Jr5WJFxNF7Y&t=205s
