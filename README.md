# elk

![elk구성도](https://user-images.githubusercontent.com/64673130/231033257-7130c0c6-21de-4e07-860c-6d3fcd47e81d.jpg)



1. ec2 생성 후 - elastic search + kibana docker container 생성

2. local에서 filebeat & logstash docker container 실행

3. logstash를 별도 서버에 구축

4. 다른 서버에서 logstash를 바라보는 filebeat 구축

5. local Mac에서 logstash로 커넥션 불가 (이유를 모르겠음) / mac은 airplay로 5000번 포트 사용

