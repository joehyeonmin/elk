# elk

elasticsearch - Elasticsearch는 Apache Lucene에 구축되어 배포된 검색 및 분석 엔진

logstash - Logstash는 다양한 소스로부터 데이터를 수집하고 전환하여 원하는 대상에 전송할 수 있도록 하는 오픈 소스 데이터 수집 도구

kibana - Kibana는 로그 및 이벤트 검토에 사용하는 데이터 시각화 및 탐색 도구

Beats - 서버에 에이전트로 설치하여 다양한 유형의 데이터를 ElasticSearch 또는 Logstash에 전송하는 오픈 소스 데이터 발송
      - filebeat.yml의 path에는 docker container의 log 경로를 적어줘야함(docker-compose volumes의 a:b -> b)

# 동작

Logstash는 데이터를 수집 및 변환하고 올바른 대상으로 전송

Elasticsearch는 수집된 데이터를 인덱싱하고, 분석하고, 검색

Kibana는 분석 결과를 시각화



(aws)


# 환경 구축

![elk구성도](https://user-images.githubusercontent.com/64673130/231033257-7130c0c6-21de-4e07-860c-6d3fcd47e81d.jpg)



1. ec2 생성 후 - elastic search + kibana docker container 생성

2. local에서 filebeat & logstash docker container 실행

3. logstash를 별도 서버에 구축

4. 다른 서버에서 logstash를 바라보는 filebeat 구축

5. local Mac에서 logstash로 커넥션 불가 (이유를 모르겠음) / mac은 airplay로 5000번 포트 사용

