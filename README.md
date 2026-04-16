<div align="center">

# 안녕하세요, 심은영입니다

### Publisher · Backend Developer · AWS Cloud

[![Tech Blog](https://img.shields.io/badge/Tech%20Blog-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://tech-notes-nu.vercel.app)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:duddl4766@gmail.com)

</div>

---

## About Me

Publisher → Backend Developer → Infrastructure
화면부터 서버, AWS 인프라까지 서비스 전체 흐름을 직접 경험했습니다.<br>
기능을 구현하기 전에 "왜 필요한가"와 "어디까지 영향이 가는가"를 먼저 묻는 게 습관입니다.

`MSA 모듈 개발` `AWS 인프라 운영` `풀스택 경험`

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

## Certifications

| 자격증 | 취득일 | 발급기관 |
|--------|--------|---------|
| 정보처리기사 | 2023.06 | 한국산업인력공단 |
| 리눅스마스터 2급 | 2024.10 | 한국정보통신진흥협회 |
| SQL 개발자 (SQLD) | 2024.04 | 한국데이터산업진흥원 |
| 웹디자인기능사 | 2020.09 | 한국산업인력공단 |

---

## IoT Platform MSA

> 스마트홈 IoT 플랫폼을 AWS 기반 MSA 구조로 전면 재설계한 프로젝트
> 1.0 상용 운영 중 · 2.0 개발 완료 단계

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


