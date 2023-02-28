# Deep Learning NLP Project
## 데이콘 소설 작가 분류 AI 경진대회
https://dacon.io/competitions/open/235670/overview/description

16기: 김진서, 노연수, 정은미
17가: 안영지 

### **Data**
    - index : 인덱스
    - text : 문장 뭉치
    - author : 작가 인덱스 값

### **2. DATA Preprocessing**
    - 불용어 처리 X
    - 표제어 추출(lemmatation)/ 어간 추출(Stem)

### **3. Modeling**
    - CNN
    - RNN 기반: lstm, gru, bi-lstm
    - 융합: Bi-lstm + CNN
    
### **4. RESULT**
    - Bi-lstm > Bi-lstm + CNN > lstm > gru > CNN
