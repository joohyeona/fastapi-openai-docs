# 📄 Doc-GPT-API

FastAPI와 OpenAI GPT API를 활용한 문서 요약 및 질의응답 API 프로젝트입니다.  
사용자가 업로드한 문서에 대해 요약을 제공하고, 문서 내용을 기반으로 자연어 질문에 응답하는 기능을 제공합니다.

---

## ✨ 주요 기능

- 📎 PDF/텍스트 문서 업로드
- ✂️ 문서 요약 자동화 (GPT 기반)
- ❓ 문서 기반 질의응답 기능 (RAG 구조)
- ⚡ FastAPI 기반 RESTful API 구성
- (선택) 🌐 간단한 웹 UI 제공

---

## 🖼️ 프로젝트 구조

project/ <br>
├── main.py # FastAPI 서버 <br>
├── utils/ <br>
│ ├── pdf_parser.py # PDF 텍스트 추출 <br>
│ └── openai_helper.py # GPT 요청 헬퍼 <br>
├── templates/ # 웹 템플릿 (선택) <br>
├── static/ # JS/CSS (선택) <br>
└── requirements.txt <br>


---

## 🚀 실행 방법

### 1. 패키지 설치
```
pip install -r requirements.txt
```

### 2. 환경 변수 설정
.env 파일 또는 환경 변수로 OpenAI API 키를 설정합니다.
```
OPENAI_API_KEY=your-api-key
```

### 3. 서버 실행
```
uvicorn main:app --reload
```

---

#### 🛠️ 기술 스택
Python 3.9+ <br>
FastAPI <br>
OpenAI GPT-3.5/4 API <br>
PyMuPDF (fitz) 또는 pdfplumber <br>
FAISS or Chroma (선택) <br>
HTML/CSS (선택 UI) <br>

---

#### 📚 예시 사용법
/upload : 문서 업로드 <br>
/summarize : 요약 생성 <br>
/ask : 질의응답 <br>

---

#### 📌 향후 개선 아이디어
문서 요약 저장 및 히스토리 관리 <br>
사용자 세션 기반 Q&A 관리 <br>
챗봇 인터페이스 통합 <br>

---

#### 📄 라이선스
MIT License
