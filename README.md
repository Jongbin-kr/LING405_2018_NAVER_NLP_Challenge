2022-1 언어와 컴퓨터(LING405) 수업에서 기말과제로 진행한 [<2018 네이버 NLP Challenge>](https://github.com/naver/nlp-challenge)의 NER(Named Entity Recognition, 개체명인식) 과제를 해결한 과정을 기록해둡니다.

세부적인 과제 해결과정은 노트북 파일을 참고하세요.

<br>

## 과제 요구사항
+ `NLTK`의 나이브 베이즈 분류기를 활용해 정확도 87% 이상의 모델을 설계할 것.
+ 모듈은 `re`, `os`, `nltk`, `Hangul.py` 모듈만 사용가능.
  + **별도의 한국어 형태소 분석기를 사용하지 말 것.**
+ 언어학적으로 적절한 특징을 설정하고, 해당 특징을 설정한 이유를 설명할 것.
+ validation set은 고려하지 말고, `test.txt`를 테스트데이터로, `train.txt`를 학습용데이터로 사용할 것.

<br>

## ⚠️주의사항⚠️
`NLTK`의 나이브베이즈분류기는 non-parametric 모델로서, 주어진 데이터의 특징들을 학습하고 가중치를 업데이트하지 않습니다. 대신 주어진 데이터 각각에 대하여 베이즈확률을 계산하고, 해당 확률값에 따라 테스트데이터에 대한 정확도를 측정합니다.

+ 출처: [NLTK naive bayes classifier documentation](https://www.nltk.org/_modules/nltk/classify/naivebayes.html) 및 [Russel, Artificial Intelligence: A Modern Approach, 2016](https://books.google.co.kr/books?id=XS9CjwEACAAJ&dq=russell+artificial+intelligence+a+modern+approach&hl=ko&newbks=1&newbks_redir=0&sa=X&redir_esc=y)