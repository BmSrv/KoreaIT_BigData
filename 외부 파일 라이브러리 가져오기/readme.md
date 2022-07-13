# 외부 패키지 설치
 ## MPG 데이터
  - MPG(Mile Per Gallon) : 1999 ~ 2008년 미국에서 출시된 자동차 연비 데이터
  - ggplot2에서 제공하는 예제 데이터

|||
|:-- |:--|
| manufacturer| 제조사|
| model | 자동차 모델명|
| displ | 배기량|
| year | 생산연도|
| cyl | 실린더 개수|
| trans | 변속기 종류|
| drv | 구동박식|
| hwy | 고속도로 연비|
| fl | 연료종류|
|class| 자동차 종류|
 
 ~~~ html
  install.packages("ggplot2")
  
  ~~~

  ~~~
  library(ggplot2)
  ~~~
  
# dplyr 데이터 전처리에 사용하는 패키지
 ~~~html
  library(dplyr)
 ~~~

  
# csv 데이터 가져오기
 ~~~html
  v1 <- read.csv("파일경로")

 ~~~

