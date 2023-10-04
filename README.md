# FakeNewsDetection

## 📌 Scikit-Learn 라이브러리를 활용해 이진 분류에 용이한 로지스틱 회귀 분석 기반 유튜브 허위 사실 탐지 모델을 개발

![image](https://github.com/harim061/FakeNewsDetection/assets/90364684/69d840bd-ae60-4222-8db2-3070da95930a)

![image](https://github.com/harim061/FakeNewsDetection/assets/90364684/9e4c8230-6766-4fc9-a404-ed67178fc39a)


## 📌 Point 
- 뉴스데이터를 사용해서 유튜브 스크립트를 판별해야해서 스크립트 전처리가 포인트
- 영어 데이터만 존재해 python에 내장된 translate 모듈 사용
- 판별에 있어 중요한 word 추출
- snuFact crawling


## 📌 Code
1. 데이터 로딩 함수 load_data
    - 주어진 경로에서 가짜 뉴스와 진짜 뉴스의 데이터를 로드합니다.
    - 두 데이터셋은 'title'과 'text' 열만 선택하여 병합되며, 레이블로 'check' 열이 추가됩니다.
    - 마지막으로 'title'과 'text' 열을 병합하여 'title_text'라는 새로운 열을 만듭니다.

2. 텍스트 전처리 함수
    - preprocessor: 기본적인 텍스트 정제 작업을 수행합니다.
    - preprocess_and_tokenize: 문장 토큰화, 단어 토큰화, 소문자화, 불용어 제거 및 기본형으로 변환 등의 작업을 수행합니다.

3. TF-IDF 벡터라이저
    - get_tfidf_vectorizer: TF-IDF 방식으로 텍스트를 벡터 형태로 변환하기 위한 벡터라이저를 반환합니다.

4. 유튜브 스크립트 전처리
    - preprocess_youtube_script: 유튜브 스크립트를 전처리합니다.
    
5. 문맥 기반 오류 검사 함수
    - context_checker와 fix_context_errors: 텍스트 내에서 문맥적 오류를 확인하고 이를 수정하는 작업을 수행합니다.
    
6. 허위 사실 탐지 함수
    - predict_fake_or_real: 주어진 뉴스 텍스트가 가짜인지 진짜인지 예측하며, 해당 예측의 확률도 반환합니다.

7. 예측 설명 함수
   - explain_prediction: 모델의 예측 결과를 기반으로, 해당 예측에 기여한 주요 단어들을 반환합니다.

- 해당 깃허브에서 확인
https://github.com/harim061/DoubleCheck_HeoSSERAFIM

- 백에 연결한 부분 
https://github.com/harim061/DoubleCheck_HeoSSERAFIM/blob/main/Project/Verify/utils.py
https://github.com/harim061/DoubleCheck_HeoSSERAFIM/blob/main/Project/Verify/views.py


