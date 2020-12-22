# lecture
Korea Univ. 자연어처리기술 기말 PJT

실행환경 : 클라우드 서버와 GPU를 제공받는 google colab, Python


## 1. 한국어 감정분석 데이터셋(NSMC)

### Overview
네이버 영화 리뷰 데이터(Naver Sentiment Movie Corpus,NSMC)를 활용하여 긍정,부정의 감정분석을 진행함

### Data
Dataset : https://github.com/e9t/nsmc

### 데이터로딩
test파일 : ko_data.csv를 .txt로 변환하여 사용하였고 컬럼명을 "Sentence"에서 "document"로 변경하여 test파일 로딩함

### Code
오픈코드 참고함 (https://github.com/jiwonny/nlp_emotion_classification)


## 2. 영어 감정분석 데이터셋(Friends)

### Overview
미국 시트콤 Friends의 대사를 annotation 투표를 통해 다수결로 정해진 emotion이 8가지로 라벨링되어 있는 데이터로 감정분석 진행함

### Data
Dataset : http://doraemon.iis.sinica.edu.tw/emotionlines/download.html
friends_dev.json, friends_test.json, friends_train.json 3개의 파일을 Friends.zip 로 압축시킨 파일을 사용함
Testset : en_data.csv 파일을 사용함

### Code
오픈코드 참고함 (https://github.com/jiwonny/nlp_emotion_classification)

### 참고site
KoBERT 참고 : https://github.com/SKTBrain/KoBERT

Friends 데이터셋 구성 : https://sites.google.com/view/emotionx2019/datasets

NSMC분석 코드참고 : https://blog.naver.com/horajjan/221739630055
