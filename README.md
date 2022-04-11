# Logos


## 유사도 기반 판례 검색 서비스

개발 인원 : 윤상운, 강규남, 김오현, 김현식, 장우영
개발 기간 : 22.01 ~ 22.02
개발 툴 : Visual Studio Code, Jupyter Notebook

### 사용 기술

Web : Django, Chart.js, amCharts

Data : Gensim, OKT, Kkma

DB : MySQL

Other : Git, Aquerytool

### 세부 내용

- 본 프로젝트의 목적은 판례 검색의 용이성을 높이는 데 있다. 일반적으로 판례 및 법규는 일상 언어와는 유리된 법률 용어로 작성되어 있는 바, 법률교육을 받지 않은 사람이 자신이 찾고자 하는 상황과 유사한 판례를 찾는 데 어려움이 있었다.
 
- 이를 AI 오픈소스 라이브러리인 Gensim을 사용하여 사용자의 검색값과 판례의 내용을 비교, 유사한 것으로 판단되는 판례를 조회하는 서비스를 기획함으로써 해소하고자 하였다.
 
- 유사도 분석 모델의 구성 및 흐름은 다음과 같다.

1. 공개된 판례 데이터 10만여 건을 크롤링, 6개의 소분야로 분류하여 DB에 저장
2. Word2Vec 모델에 영어 유의어 Datasets 학습
4. 사용자 입력값 및 판례 키워드를 영어로 번역, 모델 적용
5. 유사한 것으로 판단된 판례를 반환

- 주요 웹 기능은 다음과 같다.

1. 회원정보 CRUD
2. 판례 검색 기능
3. 3개의 커뮤니티 기능
4. 법률사전 기능
5. 자주 검색한 단어, 연관단어 등 사용자의 사용 로그에 기반한 통계 기능

