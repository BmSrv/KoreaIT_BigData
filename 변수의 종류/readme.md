# 1.변수 만들기

 * '<-' 를 사용하여 변수 생성
 * '=' 를 사용하여 변수 생성(R에서 추천하지는 않음)

~~~html
  a <- 12
  b = 5
  c <- 13.15 
  str <- "Hello World!!"
~~~
~~~ 
  # 벡터(Vector) 
   - 동일한 유형의 1차원 데이터 구조
  v <- c(1,2,3)
~~~
~~~
  # 행렬(Mrtrix)
   - 동일한 유형의 2차원 데이터 구조(행 열)
   v <- matrix(1:9, nrow=3);
~~~

# 2. 기본 연산

 * '+' 더하기
 * '-' 빼기
 * '*' 곱하기
 * '/' 나누기


# 3. 여러값으로 구성된 변수 생성하기
 
 * c() 함수 사용 (combine)
    ~~~html
    # 여러개로 이루어진 변수
    var1 <- c(1,5,10,15)
    var1 <- c('Hello','World')
    ~~~
    ~~~html
    # 콜론 ':' 1씩 증가하는 연속된 수(1~9)
    var2 <- c(1:9)
   
    ~~~
 * seq() 함수 사용
    ~~~html
     # seq() 함수 사용 (sequence)
      var3<-seq(from = 1, to =9)
    ~~~
    ~~~html
     # by 간격조절
      var4 <- seq(1, 10, by= 2) 
    ~~~
    ~~~html

     #구간 개수로 나누기
      var6 <- seq(1, 10, length= 5)
    ~~~
    ~~~
     # length 구간 나누기 
      var5 <- seq(from=1, to= 10, length= 5)
    ~~~
    ~~~
     # length.out 개수 지정
      var6 <- seq(from= 1 , by=3 , length.out=4)
    ~~~
    
    # 문자함수
    ~~~
    # paste(): 받은 인자값을 모두 합치는 함수
    paste('Hello','World')
    ~~~
    ~~~
    # collapse 구분자 추가
    str <- c('apple','orange','pear')
    paste(str, collapse=' : ')
    ~~~
    
 # 숫자를 다루는 함수
 
  * sum()
  * max()
  * min()
  * mean()
    
    
    

