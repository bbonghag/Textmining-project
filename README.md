## 텍스트마이닝을 통한 노동위원회 판정문 문서분류📑

### 노사분쟁시 노무사를 보조하기 위한 모델 개발.



---

### 📑Team
- 5명(조장 : 박재현, 조원 : 박한빈, 손보영, 이봉학)


### 📑Introduction
- 노무사로 현재 근무 중인 현직자의 아이디어로 프로젝트를 시작, 자문을 받으며 진행
- 노사분쟁중에 주로 중앙노동위원회 사이트에서 판결요지 사례들을 보며 업무를 수행하는데 이 사례에서는 기각, 인정등의 결과가 나와있으므로 어떤 단어나 문장을 사용했는지에 따라 어떤 결과가 나올지 대략 예측가능
- 하지만 판결사례의 양이 방대하여 찾아보는 과정에서 소모되는 피로도가 크다
- 이 부분을 모델을 통해 부담을 줄이고자함

<br/>

### 📑Data
- [중앙노동위원회 사이트](http://www.nlrc.go.kr/nlrc/md/search_case.go)에서 '해고'라는 키워드와 서울노동위원회 검색으로 나오는 판결요지 사례를 크롤링한 텍스트 데이터

<br/>

### 📑Methods
#### Models  
- LogisticRegression, RandomForest, LinearSVC, MultinomialNB

#### Progress
- 웹크롤링을 통한 텍스트 데이터 수집
- 데이터 전처리
  - 수집한 데이터에서 Nan값 및 불용어 제거
  - 판다스로 라벨링
  - 품사태깅으로 토큰화(벡터화)
- 머신러닝 모델링 및 학습
- 워드클라우드를 통한 단어 빈도수 시각화

<img src="https://user-images.githubusercontent.com/103362361/197949923-f9aaf579-7422-447f-b89e-1e815d301298.png"  width=50% height=50%/>

<br/>

### 📑Result
- 학습된 모델에 임의의 3문장을 넣고 어떻게 예측하는지 확인함
![실졔사례 적용예시](https://user-images.githubusercontent.com/103362361/197949006-8794151c-89b3-4d6f-80f9-320a5c07b3cc.png)
- 정답이 1,2,0인 문장을 0,2,0으로 예측

<br/>


### 📑Discussion
- 이번 프로젝트는 노사분쟁을 주제로 다루었지만 다른 법률분쟁의 판결여부까지도 확장 가능
- 이 프로젝트와 모델을 발전시킨다면 과도한 업무가 집중된 판사와 법률관련 노동자들에게 보조적인 역할을 함으로써 부담을 줄일수 있을거라 생각.

<br/>

### 📑Envs and Requirements
- Colab, Python, BeautifulSoup, Pandas, Scikit-learn


### 📑References
- http://www.nlrc.go.kr/nlrc/md/search_case.go
- https://scikit-learn.org/stable/modules/classes.html


