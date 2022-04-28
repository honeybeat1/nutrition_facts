# nutrition_facts
EDA food nutrition facts DataBase from foodsafetykorea 

## 가장 먼저 해야할 것 : 식품영양성분 지식 쌓기
![image](https://user-images.githubusercontent.com/40647396/165733505-b1178b5b-2b77-4b44-8e5a-f8e2be25323a.png)

재료(농축수산물)가 레시피를 통해 함량이 변화되어 음식으로 만들어진다. (이 과정에서 영양성분 또한 변화)




## Tidy Data
1. 각 변수는 개별의 열(column)으로 존재한다.
  - 보통 `pandas.melt`를 통해 행이 많은 데이터를 열이 많은 데이터로 펴준다. 
2. 각 관측치는 행(row)을 구성한다. 
3. 각 표는 단 하나의 관측기준에 의해서 조직된 데이터를 저장한다.
4. 만약 여러개의 표가 존재한다면, 적어도 하나 이상의 열(column)이 공유 되어야 한다. (외래키?)

### 지저분한 데이터의 일반적인 모습
1. 열 이름이(Column Header) 변수 이름이 아니고 값인 경우
2. 같은 표에 다양한 관측 단위(observational units)가 있는 경우 ex) g, mg, kcal,..
3. 혹은 하나의 관측 단위가 여러 파일로 나누어져 있는 경우
4. 하나의 열(column)에 여러 값이 들어있는 경우
5. 변수가 행과 열에 모두 포함되어 있는 경우

(참고)[Tidy Data](https://partrita.github.io/posts/tidy-data/)


### nutrition_facts 데이터셋에서 다듬을 부분
1. 같은 표에 다양한 관측 단위가 있는 부분 >> 단 하나의 관측기준에 의해서 조직된 데이터로 분할
2. 1회 제공량 100g(최소 단위)에 맞춰서 칼럼 생성



- 요리를 입력하면 필요한 재료가 장바구니에 자동으로 담기는 기능 (재료가 겹치면 더 안담기고)
