# COMP312-OperatingSystem-2020
운영체제의 핵심 기능과 알고리즘에 대한 사례를 배운다. 특히 프로세스 및 스레드 관리, 메모리 관리, I/O 장치 관리 및 파일 시스템등을 다룬다.    
또한, 리눅스 운영체제를 익히고 리눅스 기반으로 실습을 진행한다. 






### 1. Multi-Thread
> 1. int number[100]를 공유 변수로 설정한다. 초기값을 모두 0으로 한다.  
> 2. Process는 10개의 thread 연속적으로 생성한다.(for loop 이용). 
> 3. 각 thread는 다음과 같은 일을 한다.  

  thread i ( 0 <= i >= 9 ) : random() 함수를 이용해서 0에서 99 사이의 수 X 를 생성하고, number[X] 값을 1 증가 시킨다 (각 thread는 동일한 과정을 100,000번 수행). 동시에 thread I 에서 발생한 각 수의 발생 빈도 와 각 수의 발생 빈도의 합 을 구한다.  
  
> 4. 10개의 thread가 종료되면 process는 number[100]에 있는 각 수의 발생 빈도 와 이들의 총합 을 파일에 출력한다. 10개 thread에서 구한 결과 값 (각 수의 발생 빈도 와 각 수의 발생 빈도의 합 )을 각 thread별로 출력한다. 그리고 10개 thread에서 집계한 각 수의 발생 빈도를 각 수 별로 더해서 그 결과를 출력하고, 이들이 총합도 출력한다.  
> 5. random number를 생성하기 위한 seed는 시간을 이용한다 (즉, random() 함수의 매번 수행 시 다른 seed를 사용한다).  
> 6. 모든 결과는 result.dat 파일로 출력한다.  
> 7. 위과정을3번이상수행하고그결과를비교한다.  
