# 📚 AI_study — 5개월 자연어처리 학습 기록

> **Python부터 GPT까지, 60개 파일로 정리한 NLP 완전 학습**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)

---

## 📖 목차

- [프로젝트 개요](#-프로젝트-개요)
- [학습 체계](#-학습-체계)
- [파일 구성](#-파일-구성)
- [핵심 내용](#-핵심-내용)
- [어떻게 사용할까](#-어떻게-사용할까)

---

## 🎯 프로젝트 개요
 
**"Python의 기초부터 GPT까지, 자연어처리의 모든 것을 정리한 학습 저장소"**
 
- 📅 **학습 기간**: 5개월 (2025년 1월 ~ 5월)
- 📊 **파일 개수**: 60개 (매주 3개)
- 🎓 **학습 방식**: 개념 학습 + 실습 코드 + 실무 기초
- 📈 **난이도**: 초급 → 중급 → 고급
- 📌 **목적**: NLP 실무 프로젝트의 이론적 기초 마련
---

## 🏗️ 학습 체계

```
AI_study (60개 파일)

📦 1단계: Python 기초 (파일 01-22, 22개)
   ├─ 타입, 변수, 연산자
   ├─ 함수, 클래스, 모듈
   ├─ 예외 처리, 파일 I/O
   └─ 정규표현식

📦 2단계: 데이터 분석 (파일 23-27, 5개)
   ├─ NumPy (배열 연산)
   ├─ Pandas (데이터프레임)
   ├─ Matplotlib (시각화)
   └─ EDA (탐색적 데이터 분석)

📦 3단계: 머신러닝 (파일 30-37, 8개)
   ├─ 회귀 분석 (Linear, Logistic)
   ├─ 분류 (Decision Tree, Random Forest)
   ├─ 클러스터링 (K-means)
   └─ 주성분 분석 (PCA)

📦 4단계: 딥러닝 (파일 40-47, 8개)
   ├─ 신경망 (NN)
   ├─ 합성곱 신경망 (CNN)
   ├─ Keras, PyTorch
   └─ TensorFlow, tf.data.Dataset

📦 5단계: NLP 심화 (파일 48-61, 14개)
   ├─ 텍스트 전처리
   ├─ Word2Vec, 임베딩
   ├─ RNN, LSTM, GRU
   ├─ Seq2Seq 모델
   ├─ Attention, Transformer
   ├─ BERT, KoBERT
   └─ GPT (생성형 사전학습 모델)
```

---

## 📁 파일 구성

### 📦 1단계: Python 기초 (01-22)

| 파일 | 주제 | 학습 포인트 |
|------|------|-----------|
| 01~05 | 기본 문법 | print, input, 변수, 연산 |
| 06~10 | 자료구조 | 리스트, 튜플, 딕셔너리, 세트 |
| 11~15 | 제어문 | if, for, while, break, continue |
| 16~20 | 함수 & 모듈 | def, lambda, import, 내장함수 |
| 21~22 | 고급 | 예외 처리, 정규표현식 |

**예제:**
```python
# 리스트 컴프리헨션
numbers = [x**2 for x in range(10) if x % 2 == 0]

# 람다 함수
square = lambda x: x ** 2

# 정규표현식
import re
emails = re.findall(r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b', text)
```

---

### 📦 2단계: 데이터 분석 (23-27)

| 파일 | 주제 | 학습 포인트 |
|------|------|-----------|
| 23 | NumPy | 배열 생성, 연산, 브로드캐스팅 |
| 24 | Pandas | 데이터프레임, Series, 인덱싱 |
| 25 | 데이터 정제 | 결측치, 이상치, 데이터 정규화 |
| 26 | Matplotlib | 선 그래프, 막대 그래프, 히스토그램 |
| 27 | EDA | 통계 분석, 상관관계, 분포 분석 |

**예제:**
```python
import pandas as pd
import numpy as np

# 데이터프레임 생성
df = pd.DataFrame({
    'name': ['Alice', 'Bob', 'Charlie'],
    'age': [25, 30, 35],
    'salary': [50000, 60000, 75000]
})

# 결측치 처리
df.fillna(df.mean(), inplace=True)

# 그룹핑 및 집계
salary_by_age = df.groupby('age')['salary'].mean()

# 정규화 (0~1)
df['age_normalized'] = (df['age'] - df['age'].min()) / (df['age'].max() - df['age'].min())
```

---

### 📦 3단계: 머신러닝 (30-37)

| 파일 | 주제 | 학습 포인트 |
|------|------|-----------|
| 30 | 회귀 분석 | Linear Regression, 손실함수 |
| 31 | 로지스틱 회귀 | 분류, 확률 모델 |
| 32 | 결정 트리 | 정보 이득, 불순도 |
| 33 | 앙상블 | Random Forest, Gradient Boosting |
| 34 | 클러스터링 | K-means, 계층적 군집 |
| 35 | PCA | 차원 축소, 분산 설명 |
| 36 | 모델 평가 | 정확도, 정밀도, 재현율, F1 스코어 |
| 37 | 하이퍼파라미터 | GridSearchCV, CrossValidation |

**예제:**
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split, GridSearchCV

# 데이터 분할
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 모델 생성
rf = RandomForestClassifier(n_estimators=100)

# 하이퍼파라미터 튜닝
params = {
    'max_depth': [5, 10, 15],
    'min_samples_split': [2, 5, 10]
}
grid_search = GridSearchCV(rf, params, cv=5)
grid_search.fit(X_train, y_train)

# 최적 모델
best_model = grid_search.best_estimator_
```

---

### 📦 4단계: 딥러닝 (40-47)

| 파일 | 주제 | 학습 포인트 |
|------|------|-----------|
| 40 | 신경망 기초 | 퍼셉트론, 활성화 함수, 역전파 |
| 41 | CNN | 합성곱, 풀링, 이미지 분류 |
| 42 | RNN | 순환 신경망, 시계열 데이터 |
| 43 | Keras | 모델 구축, 학습, 평가 |
| 44 | PyTorch | Tensor, 자동미분, 커스텀 모델 |
| 45 | TensorFlow | Graph, Session, 최적화 |
| 46 | 정규화 | Dropout, Batch Normalization |
| 47 | 전이 학습 | Pre-trained 모델, Fine-tuning |

**예제:**
```python
import torch
import torch.nn as nn

# PyTorch로 신경망 구축
class SimpleNN(nn.Module):
    def __init__(self):
        super(SimpleNN, self).__init__()
        self.fc1 = nn.Linear(784, 128)
        self.relu = nn.ReLU()
        self.fc2 = nn.Linear(128, 10)
    
    def forward(self, x):
        x = x.view(-1, 784)
        x = self.relu(self.fc1(x))
        x = self.fc2(x)
        return x

model = SimpleNN()
criterion = nn.CrossEntropyLoss()
optimizer = torch.optim.Adam(model.parameters(), lr=0.001)
```

---

### 📦 5단계: NLP 심화 (48-61)

#### **텍스트 전처리 (파일 48-50)**

```python
import nltk
from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords

# 토큰화
tokens = word_tokenize("Natural Language Processing is amazing!")

# 불용어 제거
stop_words = set(stopwords.words('english'))
filtered_tokens = [word for word in tokens if word.lower() not in stop_words]

# 어간 추출 (Stemming)
from nltk.stem import PorterStemmer
stemmer = PorterStemmer()
stemmed = [stemmer.stem(word) for word in filtered_tokens]

# 표제어 추출 (Lemmatization)
from nltk.stem import WordNetLemmatizer
lemmatizer = WordNetLemmatizer()
lemmatized = [lemmatizer.lemmatize(word) for word in filtered_tokens]
```

#### **Word2Vec & 임베딩 (파일 51-52)**

```python
from gensim.models import Word2Vec
import numpy as np

# Word2Vec 모델 훈련
sentences = [
    ['machine', 'learning', 'is', 'awesome'],
    ['deep', 'learning', 'is', 'powerful'],
    ['artificial', 'intelligence', 'is', 'future']
]

model = Word2Vec(sentences, vector_size=100, window=5, min_count=1)

# 단어 벡터
word_vector = model.wv['machine']  # (100,) 크기 벡터

# 유사 단어 찾기
similar_words = model.wv.most_similar('learning', topn=5)
```

#### **RNN, LSTM, GRU (파일 53-54)**

```python
import torch.nn as nn

# LSTM 모델
class LSTMModel(nn.Module):
    def __init__(self, input_size, hidden_size, num_layers, output_size):
        super(LSTMModel, self).__init__()
        self.lstm = nn.LSTM(input_size, hidden_size, num_layers, batch_first=True)
        self.fc = nn.Linear(hidden_size, output_size)
    
    def forward(self, x):
        lstm_out, (h_n, c_n) = self.lstm(x)
        # 마지막 시점의 출력만 사용
        output = self.fc(lstm_out[:, -1, :])
        return output

# 시계열 예측
model = LSTMModel(input_size=10, hidden_size=50, num_layers=2, output_size=1)
```

#### **Seq2Seq & Attention (파일 55-56)**

```python
import torch
import torch.nn as nn

# 인코더-디코더 모델
class Encoder(nn.Module):
    def __init__(self, vocab_size, embedding_dim, hidden_dim):
        super(Encoder, self).__init__()
        self.embedding = nn.Embedding(vocab_size, embedding_dim)
        self.rnn = nn.LSTM(embedding_dim, hidden_dim, batch_first=True)
    
    def forward(self, src):
        embedded = self.embedding(src)
        outputs, (hidden, cell) = self.rnn(embedded)
        return hidden, cell

class Decoder(nn.Module):
    def __init__(self, vocab_size, embedding_dim, hidden_dim, output_dim):
        super(Decoder, self).__init__()
        self.embedding = nn.Embedding(vocab_size, embedding_dim)
        self.rnn = nn.LSTM(embedding_dim, hidden_dim, batch_first=True)
        self.fc = nn.Linear(hidden_dim, output_dim)
    
    def forward(self, trg, hidden, cell):
        embedded = self.embedding(trg)
        output, (hidden, cell) = self.rnn(embedded, (hidden, cell))
        logits = self.fc(output)
        return logits, hidden, cell

# 사용 예
encoder = Encoder(vocab_size=1000, embedding_dim=100, hidden_dim=256)
decoder = Decoder(vocab_size=1000, embedding_dim=100, hidden_dim=256, output_dim=1000)
```

#### **Transformer & BERT (파일 57-59)**

```python
from transformers import AutoTokenizer, AutoModel

# BERT 모델 로드
tokenizer = AutoTokenizer.from_pretrained("bert-base-uncased")
model = AutoModel.from_pretrained("bert-base-uncased")

# 텍스트 임베딩
text = "Natural Language Processing is amazing!"
inputs = tokenizer(text, return_tensors="pt")
outputs = model(**inputs)

# [CLS] 토큰의 임베딩 (문장 표현)
sentence_embedding = outputs.last_hidden_state[:, 0, :]  # (1, 768)

# KoBERT (한국어)
from transformers import AutoTokenizer, AutoModel
tokenizer_ko = AutoTokenizer.from_pretrained("skt/kobert-base-v1")
model_ko = AutoModel.from_pretrained("skt/kobert-base-v1")
```

#### **GPT & 생성 모델 (파일 60-61)**

```python
from transformers import GPT2Tokenizer, GPT2LMHeadModel

# GPT-2 모델
tokenizer = GPT2Tokenizer.from_pretrained("gpt2")
model = GPT2LMHeadModel.from_pretrained("gpt2")

# 텍스트 생성
prompt = "Natural Language Processing"
input_ids = tokenizer.encode(prompt, return_tensors="pt")

# 다음 100개 토큰 생성
output_ids = model.generate(input_ids, max_length=100, temperature=0.7)
generated_text = tokenizer.decode(output_ids[0], skip_special_tokens=True)

print(generated_text)
```

---

## 🎓 핵심 내용

### 1️⃣ **Python부터 시작하는 이유**
- 데이터 구조 이해 (리스트, 딕셔너리, 집합)
- 함수형 프로그래밍 (람다, 맵, 필터)
- 객체지향 프로그래밍 (클래스, 상속)

### 2️⃣ **데이터 분석 단계의 중요성**
- 현실의 데이터는 지저분함 (결측치, 이상치)
- EDA (탐색적 데이터 분석)로 데이터 이해
- 정규화, 스케일링으로 모델 성능 향상

### 3️⃣ **머신러닝부터 딥러닝까지의 진화**
- ML: 전통적 모델 (선형, 결정트리)
- DL: 신경망 (CNN, RNN, Transformer)
- 각 모델이 어떤 문제를 잘 푸는지 이해

### 4️⃣ **NLP의 핵심 변화**
```
Bag of Words → Word2Vec → RNN → Transformer → BERT → GPT

정적 표현     동적 표현   시계열  자기주의    사전학습  생성형
```

### 5️⃣ **각 단계별 느낀 점**
- **Python**: 문법보다 "사고의 흐름"이 중요
- **데이터 분석**: 도메인 이해가 70%, 코딩이 30%
- **ML**: 데이터 품질 > 모델 선택
- **DL**: GPU 없으면 불가능... (근데 했어요!)
- **NLP**: 최신 모델도 결국 "패턴 인식"

---

## 🚀 어떻게 사용할까

### 초급자
```
1. 파일 01~22 순서대로 풀어보기
2. 각 개념을 직접 코딩해보기
3. 예제를 수정해서 다시 실행해보기
```

### 중급자
```
1. 파일 23~37 (데이터 분석 + ML) 집중
2. 실제 데이터셋으로 프로젝트 진행
3. Kaggle 경진대회 참여
```

### 고급자
```
1. 파일 48~61 (NLP 심화) 마스터
2. Transformer 논문 읽기
3. 자신만의 모델 구현해보기
```


---

## 📞 연락처

- 📧 **Email**: byungwook.dev@gmail.com
- 📱 **Phone**: 010-4108-2302
- 🎯 **GitHub**: https://github.com/byungwook-dev

---
