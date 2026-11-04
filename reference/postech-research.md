# POSTECH 공개 강의자료·과제 조사

[첫 화면](../README.md) · [POSTECH 상세](../catalog/postech.md) · [JSON 정본](../data/postech.json) · [파일 표본 확인 기록](postech-file-checks-2026-11-04.json)

확인일: 2026-11-04. 컴퓨터공학·인공지능·수학·통계/데이터과학·산업경영공학·전자전기공학 관련 공개 자료를 찾았다. 기존 서울대·KAIST 자료에 POSTECH을 추가하고 프로젝트 이름을 **OpenCourseWare**로 반영했다. 대학 공식 운영 프로젝트가 아닌 독립 링크 카탈로그다. 해외 대학은 이후 확장 범위다.

## 집계와 포함 기준

| 분류 | 진입점 | 확인 범위 |
| --- | ---: | --- |
| 강의·과제 함께 | 3 | MOAI의 데이터공학 2026 가을·2025 가을, Programming for AX 2026 봄. 공개 강의 PDF와 실제 프로젝트 수행 지침. |
| 강의자료만 | 12 | PL 2026 봄, 컴퓨터보안 2024/2025/2026 봄, SDS 4개 수업, AI 기초 실습, 미적분 강의록, 신호 및 시스템, 이전 학기 자료구조 슬라이드. |
| 과제자료만 | 18 | 학생 과제·구현·프로젝트·보고서 보관본. 실제 문제 PDF와 학생 답안을 구분. |
| 여러 학기 혼합 | 1 | 비학점 Undergraduate AI Study의 여러 기수 발표·실습. 정규 강좌가 아님. |
| 안내·미확인 | 3 | 연속계산 2026 가을·2025 봄, 소프트웨어 취약점 분석 2026 가을의 일정·참고문헌. 실제 공개 자료 확보로 세지 않음. |
| 합계 | 37 | 고유 과목 수·학기 전체 완비·공개 웹 전수 완료를 뜻하지 않음. |

자료 항목 34개 중 단일 강좌 33개는 각각 실제 PDF·코드·노트북·HTML 표본을 확인했다. 혼합 1개도 발표 PDF 표본을 확인했다. PDF는 구조·쪽 수·EOF 및 앞 2쪽 텍스트 추출을 확인했으며 모든 쪽을 읽은 것은 아니다. 노트북은 JSON·셀 본문, 코드는 텍스트 존재만 확인했다. 과제 코드·노트북을 실행하거나 정답·점수를 검증하지 않았다. 웹 실습의 설명 HTML은 읽었으나 브라우저에서 상호작용을 실행하지 않았다. 영상 재생도 검증하지 않았다.

별도 파일/본문 요청 47개 중 46개는 정상 응답·내용 형식을 확인했다. EECE302의 오래된 Drive PDF 1개는 404여서 카탈로그에서 제외했다. 이 수치는 POSTECH의 모든 링크를 전수 검사한 수치가 아니다. 공개 기록 JSON은 URL·응답·형식·쪽 수 등의 메타데이터만 포함하며 원문 텍스트·학생 개인정보 본문·다운로드 파일은 담지 않는다. 기존 [646개 링크 재검토](recheck-2026-11-04.md)는 서울대·KAIST 조사이며 POSTECH을 검사한 기록으로 해석하지 않는다.

## 주요 원출처와 판정

- [POSTECH PL Lab 강의 목록](https://www.fpc-lab.com/courses)과 [Programming Languages 2026 봄](https://github.com/postech-pl/class-pl-26s): 실제 공개 노트는 148쪽이며 표지가 Spring 2022인 Sungwoo Park 노트를 2026 수업에서 재사용한다. 공개 `homework.md`의 과제 본문은 PLMS에 연결되므로 강의만으로 분류했다. 연속계산 저장소의 참고문헌·일정은 강의노트나 숙제 본문이 아니다. 예정된 2027 수업은 포함하지 않았다.
- [MOAI 강의 목록](https://moai.postech.ac.kr/courses.html): 세 학기별 슬라이드 2개씩과 팀 구성·수행 목표·발표·평가 기준이 적힌 프로젝트 HTML을 확인했다. “함께”의 과제 형태는 모두 `project_brief`다. 2026 가을 페이지가 제공하는 2025 기출을 2026 숙제로 세지 않았다. Programming for AX의 URL·일부 PDF에는 이전 명칭 Programming for Data Science가 남아 있어 동일 코드·학기를 근거로 연결했다.
- [CompSec Lab](https://compsec.postech.ac.kr/teaching/): CSED415의 2024/2025/2026 봄 강의 PDF는 실제 수업명·연도·본문이 확인된다. 일정의 Lab 배포·프로젝트 제안/지침 항목만으로 숙제 공개를 인정하지 않았다. CSED559 2026 가을은 안내·미확인이다.
- [Statistics & Data Science Lab](https://sds.postech.ac.kr/): 수학·베이지안·데이터마이닝·희소학습 슬라이드 PDF를 익명 공유 링크의 정상 다운로드로 확인했다. Mathematics for Data Science의 명시된 2023 Fall 갱신 슬라이드와 이전 영상은 구분한다. 나머지 개설 학기는 미상이다.
- [Sunghyun Cho 홈페이지](https://www.scho.pe.kr/)에서 연결하는 [CSED105 실습](https://sodomau.github.io/csed105-labs/): 교수의 공개 실습·시각화 데모이며 채점·제출 과제로 세지 않았다.
- [김강태 저자 페이지](https://sites.google.com/site/kangtaekim00/books): POSTECH 1학년용 Calculus 강의록의 공개 폴더·249쪽 PDF를 확인했다. 2021은 판본 연도이며 특정 수업 학기를 뜻하지 않는다. 원문의 이용 범위·저작권을 따른다. 다른 책을 임의로 POSTECH 강좌로 세지 않았다.
- [CISL 신호 및 시스템](https://sites.google.com/view/cislpostech/%ED%99%88/teaching/eece233/scheduledownload): 공개 Lecture Note #1 PDF 10쪽 확인. 2020 영상·2022 강의계획 안내가 혼재하므로 공개 노트 학기는 미상이다. 빈 Quizzes/Exams 제목은 실제 문제로 세지 않았다.
- [Seung-Hwan Baek 자료구조](https://www.shbaek.com/teaching/data-structure): 현재 페이지의 2026 봄 자료는 PLMS이며 공개 Drive 폴더는 명시적으로 이전 학기 슬라이드다. 소개 PDF 32쪽을 확인했다. 폴더 수정일 2024년을 개설 학기로 추정하지 않았다.
- [학생 학기별 과목 목록](https://github.com/choidaedae/POSTECH-CSE-Assignments): 개별 저장소 README와 이 목록으로 2021–2023 수업 학기를 확인했다. CSED490F 2023 봄 신호처리와 별도 학생의 Deep Learning Implementation은 같은 코드의 다른 주제다. 학생 구현·보고서만 있는 경우 원래 문제·공식 해설이 있다고 주장하지 않았다.
- [EECE454 2024 가을 보관본](https://github.com/jianmozhe404/POSTECH-24fall-ML-assignments)의 실제 PDF는 과목 코드·2024-10-03 마감을, [EECE372 보관본](https://github.com/ilshinHuh/POSTECH_EECE372)의 HW1은 2024 Spring을 명시한다. 학번·저장소 수정일을 수업 연도로 사용하지 않았다.

## 제외·접근 한계

로그인 PLMS는 요청하지 않았다. eTL·KLMS·Elice도 사용자 지시와 기존 수집 범위에 따라 제외한다. 공개 공유 링크의 정상 다운로드만 사용했으며 인증·접근 제한을 우회하지 않았다.

| 후보 | 이번 판단 |
| --- | --- |
| [Minsu Cho 강의 목록](https://cvlab.postech.ac.kr/~mcho/) | 수업 이력만 있고 실제 강의·과제 링크를 확인하지 못해 제외. |
| [IIL Teaching](https://iil.postech.ac.kr/teaching) | 수업명·일정 설명만 확인. 공개 자료 확보로 세지 않음. |
| [Jin Woo Jang Teaching](https://jangjw.postech.ac.kr/teaching) | 개설 이력만 확인. 공개 노트·문제 링크 미확인. |
| [Jinsu Kim 확률·통계 2021 가을](https://mathjinsukim.com/teaching/probability-statistics-2021-fall/) | POSTECH 수업임은 확인되지만 강의록·과제 본문 미확인. |
| [Jae-Hun Jung Teaching](https://sites.google.com/view/jaehunjung/teaching) | 해당 페이지의 Lecture slide 연결은 자료 파일을 직접 가리키지 않음. 이전 타 대학 수업은 제외. |
| [Jae Choon Cha 강의 페이지](https://gt.postech.ac.kr/~jccha/teaching-courses/) | 일반 요청의 인증서 검증 오류·웹 조회 실패로 원문 접근 확인 불가. 삭제·비공개라고 단정하지 않음. |
| [Sungwoo Park 이전 강의 사이트](http://pl.postech.ac.kr/~gla/cs433/) | 현재 원문 접근 확인 불가. 현 PL Lab 공개 PDF와 학생 과제 보관본은 각 출처로 분리. |
| [CISL EECE302](https://sites.google.com/view/cislpostech/%ED%99%88/teaching/eece302) 및 EECE574/577/645/646/695M/695J | EECE302의 공개 Drive 노트 표본은 404, 나머지는 실제 자료 링크 미확인. 카탈로그에 부풀려 넣지 않음. |
| [Precalculus 1](https://sites.google.com/view/precalculus1-postech) | 비학점 신입생 보충 프로그램이며 공개 본문 미확인. |
| [oxidized-postech-cs](https://github.com/sohnryang/oxidized-postech-cs) | 계획 README 위주로 실제 구현 파일을 확인하지 못해 제외. |
| [howru0321/POSTECH-CSE](https://github.com/howru0321/POSTECH-CSE) | 목차에 과목 코드 오연결·오타가 있어 단순히 목차만으로 추가하지 않음. 다른 확인 가능한 과목별 원본을 우선. |
| CSED520 Computational Imaging·CompSec의 과거 CSED702C 안내 | 비어 있는 페이지 또는 설명/일정만 확인해 별도 자료 항목으로 추가하지 않음. |
| MINDS-edu 수학·AI 프로그램 | 고교생 대상 교육 프로그램이라 이번 대학 수업 범위에서 제외. |
| GitHub 검색의 FIAP/PósTech 결과 | 브라질의 동명 교육과정이며 POSTECH 자료가 아니므로 제외. |

공개 파일의 누락·학기 불명·교수 이동·사이트 이전·검색 누락이 남을 수 있다. 현재 분류는 확인한 자료에 대한 판단이며 향후 새 공개 원문이 발견되면 기존 ID를 유지해 갱신한다.
