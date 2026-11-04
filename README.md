# OpenCourseWare

서울대·KAIST·POSTECH의 공개 강의자료와 과제를 찾고, 원하는 수업을 스스로 공부할 수 있도록 정리하는 독립 링크 카탈로그입니다. 현재 **서울대 124 · KAIST 56 · POSTECH 37, 총 217개 자료 진입점**을 정리했습니다. 이후 해외 대학으로 확장할 계획입니다.

Scott H. Young의 [MIT Challenge](https://www.scotthyoung.com/blog/myprojects/mit-challenge-2/)에서 자기주도 학습의 아이디어를 얻었습니다. MIT OpenCourseWare 또는 각 대학이 운영하거나 인증한 프로젝트는 아닙니다. 이름의 OpenCourseWare는 공개 교육자료를 모은다는 뜻이며 원문의 재배포 허가를 뜻하지 않습니다. 원문 파일을 복사하지 않고 출처 링크와 확인 기록을 관리합니다.

확인 기준일: **2026-11-04**. 서울대 최초 조사일은 2026-11-03입니다. 실제 수업 학기를 기준으로 최신순 정렬하며 미상·혼합 자료는 뒤로 둡니다. 검색되지 않는 공개 자료는 더 있을 수 있습니다.

| 학교 | 강의·과제 함께 | 강의만 | 과제만 | 혼합 | 안내·미확인 | 합계 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| 서울대 | 24 | 51 | 42 | 3 | 4 | 124 |
| KAIST | 23 | 20 | 8 | 3 | 2 | 56 |
| POSTECH | 3 | 12 | 18 | 1 | 3 | 37 |
| 합계 | 50 | 83 | 68 | 7 | 9 | 217 |

## 자료 찾기

- 학교별: [서울대](catalog/snu.md) · [KAIST](catalog/kaist.md) · [POSTECH](catalog/postech.md)
- 종류별: [강의·과제 함께](catalog/both.md) · [강의만](catalog/lectures.md) · [과제만](catalog/assignments.md) · [여러 학기 혼합](catalog/mixed.md) · [안내·미확인](catalog/unconfirmed.md)
- 순서·분야별: [전체 최신순](catalog/latest.md) · [학교·학과별](catalog/departments.md)
- JSON 정본: [SNU](data/snu.json) · [KAIST](data/kaist.json) · [POSTECH](data/postech.json)
- 조사 기록: [서울대](reference/snu-provenance.md) · [KAIST](reference/kaist-research.md) · [POSTECH](reference/postech-research.md) · [기존 두 학교 재검토](reference/recheck-2026-11-04.md)
- 관리: [분류·필드 설명](reference/methodology.md) · [추가·갱신 방법](CONTRIBUTING.md)

## 분류를 읽는 방법

**“강의·과제 함께”는 양쪽 일부가 확인됐다는 뜻입니다. 한 학기 전체 완비를 뜻하지 않으며 전체 학기 완비 검증은 현재 0개입니다.** 실제 문제, 코드 뼈대, 학생 구현·보고서, 과제 해설, 프로젝트 수행 지침을 상세 항목에서 구분합니다. 교수의 공식 자료와 학생 보관본도 따로 표시합니다. 학생 답안을 공식 정답으로 취급하지 않습니다.

POSTECH의 함께 3개는 데이터공학 2026 가을·2025 가을, Programming for AX 2026 봄의 공개 슬라이드와 팀 프로젝트 지침입니다. 학생 과제 보관본 18개와 비학점 AI 스터디 혼합 보관본 1개도 출처·한계를 표시했습니다. 자료구조의 이전 학기 슬라이드를 현재 2026년 수업 자료로 오표기하지 않았고, PLMS에만 연결된 숙제를 공개 과제로 세지 않았습니다.

서울대 함께 24에는 프로젝트 지침 2개·과제 해설만 1개가, KAIST 함께 23에는 문제해결기법의 과제 해설만 공개된 경우가 포함됩니다. 과제의 평가 비율·배포 일정·Classroom 초대만으로 실제 문제를 확보했다고 표시하지 않습니다.

진입점에는 같은 과목의 학기별 페이지와 여러 과목 보관본이 포함됩니다. 집계는 고유 과목 수와 다릅니다. 파일 구조·PDF 앞부분·HTML/코드·노트북 표본 등 항목별 확인 수준을 기록하며 모든 파일, 영상 재생, 코드 실행·정답성은 검증하지 않았습니다.

eTL은 사용자 지시로 제외했습니다. KAIST KLMS·Elice, POSTECH PLMS 등 로그인 강의실의 비공개 자료도 포함하지 않습니다. 원문의 저작권·라이선스·이용 조건은 각 출처를 따릅니다.

## 관리 방식

JSON을 정본으로 삼고 학교별·분류별·학과별·최신순 Markdown 보기를 함께 갱신합니다. 기존 ID를 보존하고 확인일·실제 학기 근거·출처·접근 제한을 기록합니다. 새 공개 자료는 Issue나 브랜치 변경으로 제안할 수 있습니다. 해외 대학은 후속 확장 범위이며 현재 집계에 포함되지 않습니다.
