## 텍스트마이닝을 통한 노동위원회 판정문 문서분류

### 노사분쟁시 노무사를 보조하기 위한 모델 개발.



---
### Description
- 노무사로 현재 근무 중인 현직자의 아이디어로 프로젝트를 시작, 자문을 받으며 진행
- 노사분쟁을 진행하면서 주로 중앙노동위원회 사이트에서 판결요지 사례들을 보며 업무를 수행하는데 이 사례에서는 기각, 인정등의 결과가 나와있으므로 어떤 단어나 문장을 사용했는지에 따라 어떤 결과가 나올지 대략 예측가능
- 하지만 판결사례의 양이 방대하여 찾아보는 과정에서 소모되는 피로도가 크다
- 이 부분을 모델을 통해 부담을 줄이고자함

### Models  
- ML Model : AdaBoost, XGB, RandomForest...+@ (후에 추가)

### Data
- [중앙노동위원회 사이트](http://www.nlrc.go.kr/nlrc/md/search_case.go)에서 '해고'라는 키워드와 서울노동위원회 검색으로 나오는 판결요지 사례를 크롤링한 텍스트 데이터

### Envs and Requirements
- Colab, Python, BeautifulSoup, Pandas, Scikit-learn

### Progress
- 웹크롤링을 통한 텍스트 데이터 수집
- 데이터 전처리
  - 수집한 데이터에서 Nan값 및 불용어 제거
  - 판다스로 라벨링
  - 품사태깅으로 토큰화(벡터화)
- 머신러닝 모델링 및 학습
- 워드클라우드를 통한 시각화

### Retrospective
- 이번 프로젝트는 노사분쟁을 주제로 다루었지만 다른 법률분쟁의 판결여부까지도 확장 가능성 존재.
- 발전시킨다면 과도한 업무가 집중된 판사와 법률관련 노동자들에게 보조적인 역할을 함으로써 부담을 줄일수 있을거라 생각.
- 

### References
- http://www.nlrc.go.kr/nlrc/md/search_case.go
- https://scikit-learn.org/stable/modules/classes.html
- 

