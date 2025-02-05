# Pill요함 (Pill-YoHam)

Welcome to **Pill요함 (Pill-YoHam)**! This project leverages advanced AI technologies and a robust backend infrastructure to provide personalized health supplement recommendations based on user health data and preferences. <br><br>

환영합니다! **Pill요함 (Pill-YoHam)** 은 첨단 AI 기술과 안정적인 백엔드 인프라를 활용하여 사용자 건강 데이터와 선호도를 기반으로 맞춤형 건강 보조제 추천 서비스를 제공합니다.

---

## 🌐 Language / 언어 선택
<details>
<summary>🇺🇸 English</summary>

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Project Structure](#project-structure)
5. [Setup](#setup)
6. [How It Works](#how-it-works)
7. [Endpoints](#endpoints)
8. [Future Improvements](#future-improvements)
9. [License](#License)

---

## Overview

This project focuses on utilizing user health data, preferences, and modern AI techniques to recommend the most suitable health supplements. The system processes stored supplement data and compares it against user input using advanced embedding models and vector similarity calculations.

---

## Features

- **Personalized Recommendations**: Tailored suggestions based on health conditions, goals, and allergies.
- **Vector-Based Similarity Matching**: High-accuracy matching using cosine similarity and embeddings.
- **RAG (Retrieval-Augmented Generation)**: Efficient use of AI models to reduce token costs and provide accurate responses.
- **Caching**: Speeds up repeated queries by storing results locally.
- **Scalable Backend**: Flask server for processing, with support for MongoDB.
- **Dynamic Data Processing**: Real-time analysis and data augmentation.

---

## Technologies Used

- **Backend**: Flask, Python
- **Database**: MongoDB
- **AI Models**: OpenAI GPT, Vector Embeddings
- **Search Augmentation**: Retrieval-Augmented Generation (RAG)
- **Web Framework**: Spring Boot (for frontend integration)
- **Frontend**: JSP, Bootstrap
- **Deployment**: Docker (optional)

---

## Project Structure

```plaintext
health-supplements/
├── ai/
│   ├── app.py                # Flask server entry point
│   ├── routes/
│   │   ├── data_routes.py    # Handles external data fetching
│   │   ├── gpt_routes.py     # AI interactions
│   │   ├── recommendation_routes.py  # Recommendation logic
│   ├── services/
│   │   ├── recommendation_service.py # Main recommendation logic
│   │   ├── embeddings_service.py     # Handles embeddings
│   │   ├── cache_service.py          # Caching layer
│   ├── utils/
│   │   ├── helpers.py                # Preprocessing and vector generation
│   │   ├── config.py                 # Configuration (API keys, DB URIs)
│   ├── models/
│   │   ├── chatgpt_integration.py    # GPT integration
│   │   ├── embeddings.py             # Embedding generation
├── web/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/supplements/ # Spring Boot backend
│   │   │   ├── resources/templates/  # JSP templates
├── README.md                         # Project documentation
├── requirements.txt                  # Python dependencies
```

---

## Setup

**Prerequisites**
- Python 3.8+
- MongoDB installed and running
- API keys for OpenAI and external health data API

---

## How It Works

**1.Data Collection**:
- Fetch health supplement data via an external API.
- Store data in MongoDB.

**2.User Input**:
- Collect user health details (e.g., age, conditions, allergies, goals).

**3.Recommendation Process**:
- Generate embeddings for user input and stored product data.
- Compare vectors using cosine similarity.
- Retrieve the top matching supplements.
- Use GPT to refine recommendations.

---

## Endpoints

**Flask Server**
1. POST /api/fetch-and-save

- Fetch and save external API data to MongoDB.

2. POST /api/generate-response

- Interact with GPT for product suggestions.

3. POST /api/recommend

- Recommend supplements based on user input.

---

## Future Improvements

- **Expand AI Model Integration**: Include Claude or other models for cost-efficiency.
- **User Authentication**: Secure login and personalized dashboards.
- **Enhanced Search**: Implement advanced filtering and sorting options.

---

## Project Retrospectives
[![Notion Icon](https://upload.wikimedia.org/wikipedia/commons/e/e9/Notion-logo.svg)](https://www.notion.so/your-notion-doc-link)

---
</details>

<details>
<summary>🇰🇷 한국어</summary>

## 목차

1. [개요](#개요)
2. [주요 기능](#주요-기능)
3. [사용 기술](#사용-기술)
4. [프로젝트 구조](#프로젝트-구조)
5. [실행](#실행)
6. [작동 방식](#작동-방식)
7. [엔드포인트](#엔드포인트)
8. [향후 개선 사항](#향후-개선-사항)
9. [라이센스](#License)

---

## 개요

**Pill요함**은 사용자 건강 데이터와 선호도를 기반으로 가장 적합한 건강 보조제를 추천하기 위해 최신 AI 기술을 활용합니다. 저장된 보조제 데이터를 처리하고 사용자의 입력과 비교하여 고급 임베딩 모델과 벡터 유사도 계산을 활용합니다.

---

## 주요 기능

- **맞춤형 추천**: 건강 상태, 목표, 알레르기에 기반한 맞춤형 추천.
- **벡터 기반 유사도 매칭**: 코사인 유사도 및 임베딩을 활용한 고정밀 매칭.
- **RAG (Retrieval-Augmented Generation)**: 효율적인 AI 모델 사용으로 비용 절감 및 정확한 응답 제공.
- **캐싱**: 반복된 요청의 결과를 로컬에 저장하여 속도 향상.
- **확장 가능한 백엔드**: MongoDB를 지원하는 Flask 서버.
- **동적 데이터 처리**: 실시간 분석 및 데이터 증강.

---

## 사용 기술

- **백엔드**: Flask, Python
- **데이터베이스**: MongoDB
- **AI 모델**: OpenAI GPT, 벡터 임베딩
- **검색 증강**: Retrieval-Augmented Generation (RAG)
- **웹 프레임워크**: Spring Boot
- **프론트엔드**: JSP, Bootstrap
- **배포**: Docker (선택 사항)

---

## 프로젝트 구조

```plaintext
health-supplements/
├── ai/
│   ├── app.py                # Flask server entry point
│   ├── routes/
│   │   ├── data_routes.py    # Handles external data fetching
│   │   ├── gpt_routes.py     # AI interactions
│   │   ├── recommendation_routes.py  # Recommendation logic
│   ├── services/
│   │   ├── recommendation_service.py # Main recommendation logic
│   │   ├── embeddings_service.py     # Handles embeddings
│   │   ├── cache_service.py          # Caching layer
│   ├── utils/
│   │   ├── helpers.py                # Preprocessing and vector generation
│   │   ├── config.py                 # Configuration (API keys, DB URIs)
│   ├── models/
│   │   ├── chatgpt_integration.py    # GPT integration
│   │   ├── embeddings.py             # Embedding generation
├── web/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/supplements/ # Spring Boot backend
│   │   │   ├── resources/templates/  # JSP templates
├── README.md                         # Project documentation
├── requirements.txt                  # Python dependencies
```
---

## 실행

**필수 조건**
- Python 3.8+
- MongoDB 설치 및 실행
- OpenAI 및 외부 건강 데이터 API 키

---

## 작동 방식

**1. 데이터 수집**:
- 외부 API를 통해 건강 보조제 데이터를 가져옵니다.
- 데이터를 MongoDB에 저장합니다.

**2. 사용자 입력**:
- 사용자 건강 정보(예: 나이, 건강 상태, 알레르기, 목표 등)를 수집합니다.

**3. 추천 프로세스**:
- 사용자 입력과 저장된 제품 데이터를 기반으로 임베딩을 생성합니다.
- 코사인 유사도를 사용하여 벡터를 비교합니다.
- 가장 일치하는 건강 보조제를 검색합니다.
- GPT를 사용해 추천을 세부적으로 조정합니다.

---

## 엔드포인트

**Flask 서버**
1. POST /api/fetch-and-save  
   - 외부 API 데이터를 가져와 MongoDB에 저장합니다.

2. POST /api/generate-response  
   - GPT와 상호작용하여 제품 추천을 생성합니다.

3. POST /api/recommend  
   - 사용자 입력에 기반하여 건강 보조제를 추천합니다.

---

## 향후 개선 사항

- **AI 모델 통합 확대**: 비용 효율성을 위해 Claude 또는 기타 모델 통합.
- **사용자 인증**: 안전한 로그인 및 개인화된 대시보드 제공.
- **고급 검색**: 고급 필터링 및 정렬 옵션 구현.

---

## 프로젝트 회고록
[![Notion Icon](https://upload.wikimedia.org/wikipedia/commons/e/e9/Notion-logo.svg)](https://www.notion.so/your-notion-doc-link)

---
</details>

## License

This project is licensed under the MIT License. See the LICENSE file for details.
