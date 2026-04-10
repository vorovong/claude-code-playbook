# Changelog

이 프로젝트의 주요 변경사항을 기록한다.
형식은 [Keep a Changelog](https://keepachangelog.com/ko/1.1.0/)를 따르며,
버전은 [Semantic Versioning](https://semver.org/lang/ko/)을 따른다.

## [Unreleased]

## [0.2.0] - 2026-04-10

### Changed

- progress 갱신 규칙: 세션 종료 의존 → 파일 변경/의사결정 시점에 즉시 기록 방식으로 전환
- progress 아카이브 규칙 추가: 100줄 초과 시 아카이브 분리 + 초기화
- CLAUDE.md 세션 프로토콜 간소화: 상세 규칙을 progress 템플릿으로 위임

## [0.1.0] - 2026-04-09

### Added

- 초기 플레이북 구조: CLAUDE.md, README, 템플릿 (progress, case-study, spec, full-project CLAUDE.md)
- Phase 1-2-3 교육 모드 체계
- 미니 프로젝트 / 풀 프로젝트 진행 규칙
- 교육 레퍼런스, 플러그인 가이드 등 docs/guides

### Changed

- README 전면 재작성 + CLI 권장 안내
- 문체 통일: 존댓말 → 기사문체(~다/~된다/~한다)

[Unreleased]: https://github.com/vorovong/claude-code-playbook/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/vorovong/claude-code-playbook/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/vorovong/claude-code-playbook/releases/tag/v0.1.0
