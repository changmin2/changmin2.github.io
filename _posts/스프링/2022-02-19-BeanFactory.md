---
title:  "스프링 기본원리(4)"

categories:
  - 스프링
tags:
  - Blog
toc: true
toc_sticky: true
---

### BeanFactory와 ApplicationContext

#### BeanFactory

- 스프링 컨테이너의 최상위 인터페이스이다.
- 스프링 빈을 관리하고 조회하는 역할을 담당
- getBean()제공
- 앞 장에서 사용한 대부분의 기능은 BeanFactory가 제공하는 기능이다.

#### ApplicationContext

- BeanFactory 기능을 모두 상속받아서 제공한다.
- 빈을 관리하고 검색하는 기능을 BeanFactory가 제공한다,
- ApplicationContext가 필요한 이유는 애플리케이션을 개발할 때는 빈을 관리하고 조회하는 기능은 물론이고, 수 많은 부가기능이 필요하기 때문이다.

![GitHub Logo](/image/ApplicationContext부가기능.png)

- 메세지소스를 활용한 국제화 기능(MessageSource) :  한국에서 들어오면 한국어로, 영어권에서 들어오면 영어로 출력
- 환경변수(EnvironmentCapable) : 로컬, 개발, 운영등을 구분해서 처리
- 애플리케이션 이벤트(ApplicationEventPublisher) : 이벤트를 발행하고 구독하는 모델을 편리하게 지원
- 편리한 리소스 조회(ResourceLoader) : 파일, 클래스패스. 외부 등에서 리소스를 편리하게 조회

-> BeanFactory나 ApplicationContext를 스프링 컨테이너라 한다.

출처 : 인프런 김영한의 스프링 핵심원리 기본편