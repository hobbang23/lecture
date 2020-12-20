# lecture
Korea Univ. 자연어처리기술 기말 PJT
실행환경 : 클라우드 서버와 GPU를 제공받는 google colab 에서 진행.


## 1. 한국어 감정분석 데이터셋(NSMC)

### Overview
네이버 영화 리뷰 데이터(Naver Sentiment Movie Corpus,NSMC)를 활용하여 한국어 감정분석을 진행함

### 분석순서
[1] 데이터 전처리
1) 라이브러리 설치 및 불러오기
2) 자료불러오기
3) 데이터 전처리 및 토큰화
4) tf_idf 기반 단어 벡터화
5) 토큰화된 단어 벡터화
6) 패딩

[2] 분석
1) 라이브러리 호출
2) 모델 컴파일(딥러닝 실행)
3) 검증

### Data
Dataset : https://github.com/e9t/nsmc

rating_train.txt: 학습 데이터 총 15만개
rating_test.txt: 테스트 데이터 총 5만개
class는 2개로 긍정, 부정으로 나뉘며 각각 분포는 50:50으로 분포되어 있음.

### Package
Tensorflow
Pandas
Numpy
re
konlpy

--------------------------------수정필요--------------------------------
### Preprocessing
데이터 전처리와 tensorflow.python.keras.prerprocessing 모듈을 이용해 index로 벡터화 진행
전처리 과정에서 전체 데이터인 ratings.txt를 사용해서 Tokenizer에 fit 
해당 객체를 이용해서 ratings_train.txt와 ratings_test.txt를 각각 index sequence 넘파이 배열로 만듦

### Training
모델은 간단한 CNN 모델을 사용함
input값을 random하게 embedding 해준뒤 tensorflow의 conv1d를 사용했고 임베딩과 convolution에 모두 dropout을 0.2의 확률로 주었음
코드는 tf.data와 tf.estimator를 사용해서 작성함

### Result
모델에는 10에폭으로 학습한다고 나와있는데, 전체 학습하지는 않고 60k step까지만 학습 후 evaluation 과 test를 진행

evaluation 결과는 다음과 같습니다.

acc = 0.8341333, global_step = 60700, loss = 0.45636088
test 데이터 결과는 다음과 같습니다.

accuracy = 83.5168 %

(다시 학습한 후 결과 update 예정)

--------------------------------(수정불요)--------------------------------
### 참고 site 
https://blog.naver.com/investgy/222017360734



## 2. 영어 감정분석 데이터셋(Friends)
### Data
Dataset : Friends.zip 로 압축시킨 파일일을 사용함

Testset : en_data.csv 파일을 사용함

### Code
오픈코드 참고함 (https://github.com/jiwonny/nlp_emotion_classification)

### 분석환경
구글 코랩 환경, Python
