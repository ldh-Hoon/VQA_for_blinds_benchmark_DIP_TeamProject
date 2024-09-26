# VQA_for_blinds_benchmark_DIP_TeamProject

저시력자 혹은 시각장애인의 물건(사물) 이미지 기반 질의응답을 위한 벤치마크 테스트 실험

### use case

가정에서, 궁금한 물건의 정보에 대한 이미지와 질문을 기반으로 한 정보 획득

#### 궁금한 물건의 정보(질문의 다양성)로 분류

- 대상이 무엇인지 분류

- 대상에 적힌 글씨(OCR)

- 대상의 개수

- 대상의 색
  
- 잘못 찍었을 경우(이미지 이슈)

- 음성인식 오류가 일어난 질문 text  

### 4(+1)가지 기능
TXT, OBJ, COL, CNT, (OTH)
텍스트 인식, 객체인식, 색, 개수, (기타)


### datasets
>촬영 시 생기는 이슈들(흔들림, 초점이 어긋남)을 포함하는 테스트 데이터셋 vizwiz(https://vizwiz.org/)

>object와 text 질문만 정제 (약 1000개)

>만약 질문에 대한 정보를 얻을 수 없으면(이미지 이슈 등으로) no / unanswerable 등으로 답변

>물건에 대한 각 질문에 대한 10개씩의 사람이 작성한 답변

>입력 text를 TTS를 통해 음성으로 변환 후 STT를 통해 오류를 만든 입력 text를 사용

### 중간 목표

- 목표 use case 탐색
- 실행 가능한 모델 탐색
- 데이터셋 설정과 완성
- 검증 코드 구현
- 결과 데이터 정리

### 모델 조사
![image](https://github.com/ldh-Hoon/VQA_for_blinds_benchmark_DIP_TeamProject/assets/139981434/4b75bddc-5bd9-4bfe-8b24-50d0d809f70e)

![image](https://github.com/ldh-Hoon/VQA_for_blinds_benchmark_DIP_TeamProject/assets/139981434/7a6e0fce-3856-4fab-9245-c44f39801ad9)

### 성능 평가

종합 

![image](https://github.com/ldh-Hoon/VQA_for_blinds_benchmark_DIP_TeamProject/assets/139981434/31b70b53-74df-4ac6-b5c0-8c6b724a18b2)


정확도
![image](https://github.com/ldh-Hoon/VQA_for_blinds_benchmark_DIP_TeamProject/assets/139981434/f2fada16-509a-4a34-b71d-c4bdd589367a)

-task 영역별

![image](https://github.com/ldh-Hoon/VQA_for_blinds_benchmark_DIP_TeamProject/assets/139981434/c41c8a39-9253-42ad-8187-2fb50972b33c)

-이미지 이슈 & 음성인식 질문

![image](https://github.com/ldh-Hoon/VQA_for_blinds_benchmark_DIP_TeamProject/assets/139981434/38fdbbe6-48a9-482e-86b9-4520386e0359)

-속도(전체 걸린시간)
![image](https://github.com/ldh-Hoon/VQA_for_blinds_benchmark_DIP_TeamProject/assets/139981434/b58c7f49-1468-4dfc-8020-28545ba6111f)


