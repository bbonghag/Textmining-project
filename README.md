## 텍스트마이닝을 통한 노동위원회 판전문 문서분류

### 노무관련 소송시 법률 자문 자료를 찾을때 보조하기 위한 모델 개발.



---
### Description
- 노무사로 현재 근무 중인 현직자의 아이디어 및 자문 

### Models  
- ML Model : AdaBoostClassifier, XGBClassifier, RandomForestClassifier

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
-

### References
- http://www.nlrc.go.kr/nlrc/md/search_case.go
- https://scikit-learn.org/stable/modules/classes.html
- 

