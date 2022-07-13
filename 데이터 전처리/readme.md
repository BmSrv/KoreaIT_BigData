# 데이터 전처리

 * dplyr 패키지 사용
    
    ~~~html
    library(dplyr)
    ~~~
    
    ||||||
    |:-|:-|:-|:-|:-|
    |id|class|math|english|science|
    |1   |1   |50   |98   |50   |
    |2   |1   |60   |97   |60   |
    |3   |1   |45   |86   |78   |
    |4   |1   |30   |98   |58   |
    |5   |2   |25   |80   |65   |
    |6   |2   |50   |89   |98   |
    
# dplyr 패키지 함수

* filter() 조건에 맞는 행 데이터 추출

   - df_std %>% filter(class==1)
    
    
   ||||||
   |:-|:-|:-|:-|:-|
   |id|class|math|english|science|
   |1   |1   |50   |98   |50   |
   |2   |1   |60   |97   |60   |
   |3   |1   |45   |86   |78   |
   |4   |1   |30   |98   |58   |
   
   - df_std %>% filter(class%2==0)
    
    
    ||||||
    |:-|:-|:-|:-|:-|
    |id|class|math|english|science|
    |2   |1   |60   |97   |60   |
    |4   |1   |30   |98   |58   |
    |6   |2   |50   |89   |98   |
    
   - df_std %>% filter(math>50 & english >50 & science > 50)
   
    ||||||
    |:-|:-|:-|:-|:-|
    |id|class|math|english|science|
    |1   |1   |50   |98   |50   |
    |2   |1   |60   |97   |60   |
    
    
* select() 필요한 열 데이터 추출

    - df_std %>% select(math)

    ||
    |:-|
    |math|
    |50   |
    |60   |
    |45   |
    |30   |
    |25   |
    |50   |
    
    - df_std %>% select(-math)

   |||||
   |:-|:-|:-|:-|
   |id|class|english|science|
   |1   |1     |98   |50   |
   |2   |1     |97   |60   |
   |3   |1     |86   |78   |
   |4   |1     |98   |58   |
   
   - df_std %>% select(class, math, science)

   ||||
   |:-|:-|:-|
   |class|math|science|
   |1   |50 |50   |
   |1   |60 |60   |
   |1   |45 |78   |
   |1   |30 |58   |

* arrange() 정렬

* mutate() 변수 추가

* summarise() 통계치 분석

* group_by() 집단별로 나누기

* left_join() 데이터 합치기(열)

* bind_rows() 데이터 합치기(행)

