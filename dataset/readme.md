### vizwiz object/text 관련 이미지로만 정제

https://colab.research.google.com/drive/11gmC65Fn_Q6GqnUVnsCzRjSY59-9-Be1?authuser=3#scrollTo=Tn3DKhCiCLQl

output.json : 1000개

구글 드라이브에 다운로드하는 코랩 : https://colab.research.google.com/drive/1wSFIiW0IRMO5hD6jyPB2SHkRO6x-XR1X?usp=sharing

<details>
    <summary>정제 방식</summary>


    Annotations, train.json (https://vizwiz.org/tasks-and-datasets/vqa/) 과 
    
    vision skill Annotations csv파일( https://vizwiz.org/tasks-and-datasets/vision-skills/)을 사용하여 text or object task인 데이터로 좁히기
    

</details>

<details>
    <summary>json 형식</summary>

```XML
[
  {
    "image": "VizWiz_train_00000000.jpg",
    "question": "What's the name of this product?",
    "answers": [
      { "answer_confidence": "yes", "answer": "basil leaves" },
      { "answer_confidence": "yes", "answer": "basil leaves" },
      { "answer_confidence": "yes", "answer": "basil" },
      { "answer_confidence": "yes", "answer": "basil" },
      { "answer_confidence": "yes", "answer": "basil leaves" },
      { "answer_confidence": "yes", "answer": "basil leaves" },
      { "answer_confidence": "yes", "answer": "basil leaves" },
      { "answer_confidence": "yes", "answer": "basil leaves" },
      { "answer_confidence": "yes", "answer": "basil leaves" },
      { "answer_confidence": "yes", "answer": "basil" }
    ]
  },
  {
    "image": "VizWiz_train_00000023.jpg",
    "question": "What is this movie?",
    "answers": [
      { "answer_confidence": "yes", "answer": "brides maids" },
      { "answer_confidence": "yes", "answer": "brides maids" },
      { "answer_confidence": "yes", "answer": "bridesmaids" },
      { "answer_confidence": "yes", "answer": "bridesmaids" },
      { "answer_confidence": "yes", "answer": "bridesmaids" },
      { "answer_confidence": "yes", "answer": "brides maids" },
      { "answer_confidence": "yes", "answer": "brides maids" },
      { "answer_confidence": "yes", "answer": "brides maid" },
      { "answer_confidence": "no", "answer": "unanswerable" },
      { "answer_confidence": "yes", "answer": "brides maids" }
    ]
  },

.
.
.
]
```

</details>


<details>
    <summary>기존 데이터 분포(중복 있음)</summary>

text, object, color, count, other

TXT, OBJ, COL, CNT, OTH

[9705, 14217, 10462, 1585, 863]

</details>


<details>
    <summary>정제 후 데이터 포(중복 있음)</summary>

text, object, color, count, other

TXT, OBJ, COL, CNT, OTH

[772, 999, 703, 233, 200]

</details>
