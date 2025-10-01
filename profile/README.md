# Mango

> 금융 소비 데이터를 기반으로, 나와 진심이 맞는 사람을 찾아주는 소개팅 서비스

<div align="center">

<!-- 로고 이미지 추가 -->
<!-- ![로고](이미지URL) -->

[![GitHub stars](https://img.shields.io/github/stars/조직명/저장소명?style=social)](링크)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](링크)

[🌐 홈페이지](링크) • [📱 데모](링크) • [📖 문서](링크)

</div>

## 🎯 프로젝트 소개

실제 금융 소비 데이터를 분석하여 진정한 취향 궁합을 찾아주는 AI 기반 매칭 서비스입니다.

## 👥 팀 구성

<table>
<tr>
<td align="center" width="33%">
<img src="https://github.com/IMCTZN.png" width="120" height="120" style="border-radius: 50%;">
<br/>
<b>박심인</b>
<br/>
<i>Frontend</i>
<br/>
<a href="https://github.com/IMCTZN">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/>
</a>
</td>
<td align="center" width="33%">
<img src="https://github.com/skdbsqls.png" width="120" height="120" style="border-radius: 50%;">
<br/>
<b>나윤빈</b>
<br/>
<i>Frontend</i>
<br/>
<a href="https://github.com/skdbsqls">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/>
</a>
</td>
<td align="center" width="33%">
<img src="https://github.com/Klomachenko.png" width="120" height="120" style="border-radius: 50%;">
<br/>
<b>이규민</b>
<br/>
<i>AI & Frontend</i>
<br/>
<a href="https://github.com/Klomachenko">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/>
</a>
</td>
</tr>
<tr>
<td align="center" width="33%">
<img src="https://github.com/hongdaestreet.png" width="120" height="120" style="border-radius: 50%;">
<br/>
<b>주홍대</b>
<br/>
<i>Backend</i>
<br/>
<a href="https://github.com/hongdaestreet">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/>
</a>
</td>
<td align="center" width="33%">
<img src="https://github.com/SoTaeHo.png" width="120" height="120" style="border-radius: 50%;">
<br/>
<b>👑 소태호 👑</b>
<br/>
<i>Backend</i>
<br/>
<a href="https://github.com/SoTaeHo">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/>
</a>
</td>
<td align="center" width="33%">
<img src="https://github.com/blueconecell.png" width="120" height="120" style="border-radius: 50%;">
<br/>
<b>김정연</b>
<br/>
<i>Infra & Backend</i>
<br/>
<a href="https://github.com/blueconecell">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/>
</a>
</td>
</tr>
</table>

### 주요 기능

1. **자동 프로필 생성**

   - 결제 데이터 분석으로 대표유형과 개인 키워드 자동 산출
   - 긴 자기소개 작성 불필요

2. **AI 맞춤 매칭**

   - 점수 기반 정량적 매칭
   - 퍼센트와 점수로 명확한 궁합 표시

3. **소비패턴 궁합 분석**

   - 상위 매칭 상대 추천
   - 소비패턴 궁합 그래프 시각화

4. **개인 소비 분석**
   - 내 소비패턴 인사이트 제공
   - 그래프 기반 직관적 분석

## ✨ 핵심 차별점

### 🔹 실제 데이터 기반 분석

기존 소개팅 앱의 선호도 설문이나 프로필 기반과 달리, **실제 금융 소비 데이터**로 성향을 분석합니다.

### 🔹 딥러닝 시퀀스 학습

단순 분석이 아닌 **GRU 시퀀스 모델**로 소비 흐름(순서, 주기, 빈도)까지 반영합니다.

### 🔹 정교한 매칭 알고리즘

코사인 유사도와 유저 임베딩을 조합해 대표유형 + 키워드 + 유사도를 종합한 최종 점수를 산출합니다.

### 🔹 설명 가능한 AI

임베딩/유사도 기반 매칭 결과를 **사람이 이해할 수 있는 키워드/유형**으로 제공합니다.

## 🏗️ 시스템 아키텍처

### 기술적 특징

**1. 마이데이터 최적화**

- Rate limit를 고려한 유사 캐시 방식 구현
- DB 우선 조회 후 금융망 요청으로 효율성 극대화

**2. 소비 로그 시퀀스 학습**

- GRU 기반 모델로 결제 로그 시퀀스 학습
- 시간적 전이와 주기성까지 반영한 소비 임베딩 생성
- 단순 라벨 분류를 넘어선 의미 좌표계 구축

**3. 대표유형 & 키워드 자동 산출**

- 코사인 유사도로 유저 벡터와 소비 항목 비교
- 유형별 키워드 세트 매핑으로 대표유형 확률 분포 생성
- 딥러닝 임베딩 기반 정확한 성향 추출

**4. 정교한 매칭 점수 산출**

- 대표유형 + 키워드 벡터 종합 분석
- 선호/비선호 분리: 공통 선호 가산, 공통 비선호 보정
- 매칭 점수, 퍼센트, 순위 자동 산출

**5. 설명 가능한 추천**

- 매칭 근거가 되는 공통 키워드 추출
- "둘 다 카페를 즐겨요" 등 직관적 피드백 제공
- 확장 가능: 장소 추천, 상권 연계 등

## 🛠️ 기술 스택

### Frontend - Mobile

![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)

- **Framework**: React Native (Expo)
- **Language**: TypeScript
- **State Management**: Tanstack Query, Zustand
- **Styling**: NativeWind
- **Version**: React Native 0.81

### Frontend - Web (Landing)

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)

- **Framework**: React
- **Language**: TypeScript
- **Styling**: Tailwind CSS

### Backend

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Java](https://img.shields.io/badge/Java_21-007396?style=flat-square&logo=openjdk&logoColor=white)

- **Frameworks**: Spring Boot, FastAPI
- **Language**: Java 21

### AI/ML

![Python](https://img.shields.io/badge/Python_3.13-3776AB?style=flat-square&logo=python&logoColor=white)

- **Language**: Python 3.13
- **Model**: GRU 기반 시퀀스 학습

### Database & Cache

![MySQL](https://img.shields.io/badge/MySQL_8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

- **RDB**: MySQL 8.0.42
- **NoSQL**: MongoDB
- **Cache**: Redis

## 📦 저장소

- 🎨 [Frontend Mobile](저장소링크)
- 🌐 [Frontend Web](저장소링크)
- ⚙️ [Backend API](저장소링크)
- 🤖 [AI Model](저장소링크)

## 🚀 시작하기

```bash
# 각 저장소의 README를 참고하세요
```

## 📄 라이선스

이 프로젝트는 [MIT 라이선스](LICENSE) 하에 있습니다.

## 📞 문의

- **Email**: contact@example.com
- **Team Notion**: [노션 링크](링크)

---

<div align="center">

**Made with ❤️ by [팀명]**

⭐ 이 프로젝트가 마음에 드셨다면 Star를 눌러주세요!

</div>
