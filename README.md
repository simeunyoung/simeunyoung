<div align="center">

# 안녕하세요, 심은영입니다

### Backend Developer · IoT Platform · AWS Cloud

[![Tech Blog](https://img.shields.io/badge/Tech%20Blog-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://tech-notes-nu.vercel.app)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:duddl4766@gmail.com)

</div>

---

## About Me

```
백엔드 개발과 인프라 운영을 함께 다루는 개발자입니다.

스마트홈 IoT 플랫폼 프로젝트에서
인증 서버 · 알림 서비스 · 자동화 이벤트 엔진을 직접 설계 및 구현하였고
디바이스 제어 모듈과 AWS 인프라는 인계받아 운영 개선을 주도했습니다.

단순히 기능을 구현하는 것에서 나아가,
시스템 전체의 흐름을 이해하고 서비스 품질을 함께 개선하는 것을 목표로 합니다.
```

---

## Tech Stack

**Backend**

![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.2-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security_6-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Spring WebFlux](https://img.shields.io/badge/Spring_WebFlux-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Quartz](https://img.shields.io/badge/Quartz_Scheduler-FF6B35?style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

**Database & ORM**

![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![JPA](https://img.shields.io/badge/JPA_Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-0769AD?style=flat-square)

**AWS**

![EC2](https://img.shields.io/badge/EC2-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![RDS](https://img.shields.io/badge/RDS-527FFF?style=flat-square&logo=amazonaws&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazons3&logoColor=white)
![Lambda](https://img.shields.io/badge/Lambda-FF9900?style=flat-square&logo=awslambda&logoColor=white)
![IoT Core](https://img.shields.io/badge/IoT_Core-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![API Gateway](https://img.shields.io/badge/API_Gateway-FF4F8B?style=flat-square&logo=amazonaws&logoColor=white)
![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=flat-square&logo=amazonaws&logoColor=white)
![CloudTrail](https://img.shields.io/badge/CloudTrail-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![CloudFront](https://img.shields.io/badge/CloudFront-8C4FFF?style=flat-square&logo=amazonaws&logoColor=white)
![IAM](https://img.shields.io/badge/IAM-DD344C?style=flat-square&logo=amazonaws&logoColor=white)
![ALB](https://img.shields.io/badge/ALB-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![EventBridge](https://img.shields.io/badge/EventBridge-FF4F8B?style=flat-square&logo=amazonaws&logoColor=white)

**Infra & DevOps**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-3C5280?style=flat-square&logo=mqtt&logoColor=white)
![FCM](https://img.shields.io/badge/Firebase_FCM-FFCA28?style=flat-square&logo=firebase&logoColor=black)

---

## DAMDA 2.0 — IoT Platform MSA

> 스마트홈 IoT 플랫폼을 AWS 기반 MSA 구조로 전면 재설계한 프로젝트

```
┌──────────────────────────────────────────────────────────────────┐
│                       DAMDA 2.0 Architecture                     │
├──────────────┬───────────────┬────────────────┬──────────────────┤
│  OAuth2 서버 │  Membership    │     Push      │       Event      │
│  JWT 중앙인증 │  회원 · 그룹   │ FCM 푸시알림    │   이벤트 엔진    │
└──────────────┴───────────────┴────────────────┴──────────────────┘
                          ↕  AWS IoT Core / MQTT
┌──────────────────────────────────────────────────────────────────┐
│         DeviceControl  ·  Data  ·  Lambda                        │
│          디바이스 제어    IoT 데이터 수집   이벤트 라우팅 / OTA    │
└──────────────────────────────────────────────────────────────────┘
         Java 17 · Spring Boot 3.2.5 · MariaDB (AWS RDS)
```

| 모듈 | 핵심 구현 포인트 |
|------|----------------|
| **OAuth2 서버** | Spring Authorization Server · RSA JWK DB 영속화 · 기기 단위 로그아웃 · PKCE |
| **Membership** | SMS 인증 · 그룹 초대 시스템 · MDC traceId 분산 로그 추적 |
| **Firebase Push** | Firebase 토큰 자동 갱신/무효화 · WebClient 비동기 · UPSERT Native SQL |
| **Event** | Quartz 스케줄러 · Spring ApplicationEvent 비동기 분리 · 멀티 데이터소스 |
| **Device Control** | AWS IoT Core · MQTT/TLS · Saga 보상 트랜잭션 · OTA 펌웨어 업데이트 |
| **Lambda** | OTA 폴링 → MQTT 이벤트 드리븐 전환 · Lambda 역할 분리 |

---

## Problem Solving Highlights

| 구분 | 요약 |
|------|------|
| EC2 부팅 실패 | Xen 하이퍼바이저 CONSOLE_EVTCHN 오류 → t3(Nitro) 마이그레이션 권고 |
| OAuth2 JWT 이중화 | Sticky Session 구조의 한계 인지 → JWK DB 영속화로 무중단 배포 가능 구조 전환 |
| OTA 상태 반영 지연 | EventBridge 폴링 구조 → MQTT 이벤트 드리븐으로 전환, 즉시 반영 |
| CloudFront 캐시 미갱신 | 동일 파일명 교체 시 CDN 캐시 문제 → 타임스탬프 파일명 전략 적용 |
| 서버 파일시스템 과점유 | 고아 로그 원인 분석 → logrotate 전 서버 표준화 (93% → 46%) |

> 상세한 분석과 해결 과정은 **[Tech Notes](https://tech-notes-nu.vercel.app)** 에 기록하고 있습니다.

---

## Tech Notes

> 실무에서 겪은 문제 해결 과정과 시행착오를 기록하는 개발 블로그

[![Tech Blog](https://img.shields.io/badge/tech--notes--nu.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://tech-notes-nu.vercel.app)

`spring-boot` `backend` `infra` `server` `troubleshooting` `git` `devops` `logging`

---

## Certifications

| 자격증 | 취득일 | 발급기관 |
|--------|--------|---------|
| 정보처리기사 | 2023.06 | 한국산업인력공단 |
| 리눅스마스터 2급 | 2024.10 | 한국정보통신진흥협회 |
| SQL 개발자 (SQLD) | 2024.04 | 한국데이터산업진흥원 |
| 웹디자인기능사 | 2020.09 | 한국산업인력공단 |

---

<div align="center">

*"단순히 주어진 일만 수행하기보다, 관련된 시스템 구조와 다른 팀의 업무 흐름까지 함께 이해하려 노력했습니다."*

</div>
