# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

유명한 명언을 보여주는 단일 페이지 웹 애플리케이션입니다. 모든 애플리케이션 코드는 `index.html` 파일 하나에 포함되어 있으며, CSS와 JavaScript가 임베디드 형태로 작성되어 있습니다.

## 아키텍처

**단일 파일 구조**: 모든 HTML, CSS, JavaScript가 `index.html`에 포함됨:
- CSS는 `<head>` 섹션의 `<style>` 태그 안에 작성 (7-147줄)
- JavaScript는 `<body>` 끝부분의 `<script>` 태그 안에 작성 (160-266줄)
- 명언 데이터는 JavaScript 객체 배열인 `quotes` 상수에 저장 (161-242줄)

**핵심 컴포넌트**:
- 명언 데이터 구조: 각 명언 객체는 `text`와 `author` 속성을 가짐
- 상태 관리: 전역 변수 `currentIndex`와 `viewedCount`로 명언 표시 상태 추적
- 랜덤 선택 로직: `showNewQuote()` 함수를 통해 연속으로 같은 명언이 나오지 않도록 보장

## 애플리케이션 실행

`index.html` 파일을 최신 웹 브라우저에서 직접 열면 됩니다. 빌드 과정, 서버, 의존성 설치가 필요 없습니다.

## 수정 방법

**명언 추가/수정**: JavaScript 섹션의 `quotes` 배열을 수정 (161-242줄). 각 항목은 반드시 `text`와 `author` 속성을 가져야 합니다.

**스타일 수정**: `<style>` 섹션의 CSS를 수정 (7-147줄). 모바일 기기용 반응형 브레이크포인트는 768px입니다.

**언어**: 모든 사용자 인터페이스 텍스트는 한국어로 작성되어 있습니다. 페이지는 `lang="ko"` 속성을 사용합니다.
