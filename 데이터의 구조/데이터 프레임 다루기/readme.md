# 데이터 프레임 (DataFrame)
  - 데이터 유형에 관계없는 2차원 데이터구조
  - 엑셀 스프레드 시트와 같은 형태
  ~~~html
  name <- c('jms','tjm','bms')
  age <- c(23,25,25)
  score <- c(123,456,789)
  d_f <- data.frame(name, age, score)
  ~~~
  ||||
  |:-|:-|:-|
  |name|age|score|
  |'jms'|23|123|
  |'tjm'|25|456|
  |'bms'|25|789|

# 데이터 프레임에 열 추가
  
  - d_f <- data.frame(추가할 프레임, 추가할 데이터)
    
   ~~~html
        d_f<- dataframe(d_f,num=c(1,2,3))
   ~~~
   |||||
  |:-|:-|:-|:-|
  |name|age|score|num|
  |'jms'|23|123|1|
  |'tjm'|25|456|2|
  |'bms'|25|789|3|
  
  
      
# 변수명 바꾸기
  - rename(데이터 프레임, 새 변수명 = 기존 변수명)
  ~~~html
  
  d_f <- rename(d_f, score=math_score)
  
  ~~~
  |||||
  |:-|:-|:-|:-|
  |name|age|math_score|num|
  |'jms'|23|123|1|
  |'tjm'|25|456|2|
  |'bms'|25|789|3|

  
# 파생 변수
  //영어점수 추가
  d_f <- data.frame(d_f,english_score=c(321,654,987))
  
  ||||||
  |:-|:-|:-|:-|:-|
  |name|age|math_score|num|english_score|
  |'jms'|23|123|1|321|
  |'tjm'|25|456|2|654|
  |'bms'|25|789|3|987|
  
  ~~~html
  d_f$mean_score <- (d_f$math_score+d_f$english_score)/2
  ~~~
  
  |||||||
  |:-|:-|:-|:-|:-|:-|
  |name|age|math_score|num|english_score|mean_score|
  |'jms'|23|123|1|321|222|
  |'tjm'|25|456|2|654|555|
  |'bms'|25|789|3|987|888|
  
# 조건문으로 파생변수 생성
  ~~~html
    d_f$old <- ifelse(d_f$age>24,"True","False")
  ~~~
  ||||||||
  |:-|:-|:-|:-|:-|:-|:-|
  |name|age|math_score|num|english_score|mean_score|old|
  |'jms'|23|123|1|321|222|False|
  |'tjm'|25|456|2|654|555|True|
  |'bms'|25|789|3|987|888|True|
  
# 데이터 프레임 함수
  
   - head()
     - 데이터 앞부분 출력
   - tail()
      - 데이터의 뒷부분 출력
   - view()
      - 뷰어창에서 데이터 확인
   - dim()
      - 데이터 차원 출력
        ~~~html
          20'5
        ~~~
      
   - str()
      - 데이터 속성 출력
        ~~~html
          'data.frame':	20 obs. of  5 variables:
          $ id     : int  1 2 3 4 5 6 7 8 9 10 ...
          $ class  : int  1 1 1 1 2 2 2 2 3 3 ...
          $ math   : int  50 60 45 30 25 50 80 90 20 50 ...
          $ english: int  98 97 86 98 80 89 90 78 98 98 ...
          $ science: int  50 60 78 58 65 98 45 25 15 45 ...
        ~~~
   - summary()
      - 요약통계량 출력
      ~~~html
         id            class        math          english        science     
         Min.   : 1.00   Min.   :1   Min.   :20.00   Min.   :56.0   Min.   :12.00  
         1st Qu.: 5.75   1st Qu.:2   1st Qu.:45.75   1st Qu.:78.0   1st Qu.:45.00  
         Median :10.50   Median :3   Median :54.00   Median :86.5   Median :62.50  
         Mean   :10.50   Mean   :3   Mean   :57.45   Mean   :84.9   Mean   :59.45  
         3rd Qu.:15.25   3rd Qu.:4   3rd Qu.:75.75   3rd Qu.:98.0   3rd Qu.:78.00  
         Max.   :20.00   Max.   :5   Max.   :90.00   Max.   :98.0   Max.   :98.00  
      ~~~
  
  
