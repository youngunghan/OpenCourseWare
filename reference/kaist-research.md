# KAIST 조사 범위와 주의할 항목

> 2026-11-04 게시본 재검토에서 일부404 링크를 분리하고 CS580 이전 주소·Agentic AI의 공식성 표현을 수정했다. 항목 수·분류 집계는 불변이며 [재검토 기록](recheck-2026-11-04.md)과 링크별 결과가 현재 접근 한계를 보완한다.

확인일: 2026-11-04. 전산학부, 수리과학과·수리통계 관련, 산업및시스템공학과, 전기및전자공학부, AI컴퓨팅·김재철AI대학원 관련 공개 자료를 조사했다. 통계는 독립 학과로 가정하지 않고 실제 자료의 개설 과목·학과에 따라 표시한다. DS801은 데이터사이언스대학원 관련으로 구분했다.

56개 진입점은 함께 23, 강의만 20, 과제만 8, 혼합 3, 자료 미확인 2다. 실제 수업의 여러 학기판은 별도 항목이고 한 수학 노트 저장소는 과목별 8개 폴더로 나눴다. 따라서 고유 과목 수나 인터넷 전수조사 완료 수가 아니다. 전체 학기 완비 확인은 0이다.

공식 수업 페이지의 학기·자료 목록, 공개 GitHub README와 재귀 파일 트리, 강의·과제 PDF 표본 앞부분, 실제 TODO 노트북·공개 뼈대를 대조했다. 영상은 수업 페이지의 공개 녹화 링크를 확인했으며 영상 전체 재생을 검증하지 않았다. OneDrive/SharePoint 슬라이드 전부의 익명 다운로드도 검증하지 않았다. GitHub 기본 브랜치 자료는 갱신될 수 있어 과거 배포 버전과 동일성을 보장하지 않는다. 제출 시스템 KLMS·개인 Classroom 저장소·Elice 로그인 자료는 조사하지 않았다.

## 분류에 영향을 준 확인

| 대상 | 근거와 처리 |
| --- | --- |
| [AIC313/CS378 2026 가을](https://generative-models.kaist.ac.kr/) | 공식 공개 녹화와 [FastGen 수행 지침](https://generative-models.kaist.ac.kr/fastgen/)·기본 코드 링크. 발표 예정 일정만으로 자료를 추가하지 않았다. |
| [CS479 2026 봄](https://3dml.kaist.ac.kr/) | [과제 페이지](https://3dml.kaist.ac.kr/programming-assignments/)의 PointNet 등 실제 문제·뼈대. 선택 NeRF Applications 세션을 정규 과제로 합치지 않았다. |
| [CS492(C) 2025 가을](https://diffusion.kaist.ac.kr/) | DDPM/DDIM 노트북 안의 Task·TODO·제출 지침 확인. 선택 Demo 세션은 숙제와 구분. |
| [문제해결기법 2026 가을](https://ohtae.in/teaching/) | 조교 PDF 표지와 HW1 풀이 본문. 함께 분류의 과제 측은 해설이며 원 문제 전체 확보가 아니다. |
| [DS801](https://dabeenl.github.io/DS801) | 공식 페이지·과제2는 Spring 2024, 강의1 표지의 Fall 2024와 날짜 2024-02-26은 충돌한다. 공식 페이지 기준 봄으로 정렬하고 충돌을 표시했다. assignment1.pdf는 HTTP200·application/pdf지만 실제 본문은 0바이트. 실제 문제가 읽히는 assignment2.pdf를 사용했다. |
| [CS20200 2026 봄](https://softsec.kaist.ac.kr/courses/2026s-cs20200/) | 현재 Main README 연결과 공개 Homework5/7/8 문제·IMPLEMENT 뼈대 확인. 과거 학기 Main 링크가 현재 자료를 가리키므로 과거 과제까지 소급 인정하지 않았다. |
| [EE209 2026 가을](https://kaist-ee209.github.io/) | 과제1~3의 실제 HTML 문제·뼈대 링크. 강의 일정·외부 참고 매뉴얼은 강의자료로 세지 않았고 과거 EE485 ZIP을 현재 학기에 합치지 않았다. |
| [IE437](https://github.com/omeletJK/ie437) | 공개 강의 Markdown과 프로젝트 수행 지침. syllabus의 2025 Fall과 공지의 2026 날짜가 충돌해 학기 미상으로 분리. |
| [수학 개인 노트](https://github.com/A-H4NU/kaist-math-notes) | PDF·TeX 표본. 표지 작성일은 개설 학기가 아니다. MAS212 폴더/표지 MAS242 충돌과 중도 작성 자료를 표시했다. |

## 확인했으나 본 자료 집계에 넣지 않은 범위

| 출처 | 이유 |
| --- | --- |
| [AI505/AI801 최적화](https://ai-505.github.io/assignments/preface_1/) | 과목번호가 비슷하지만 실제 지침·교수·제출 안내는 덴마크 SDU 수업. KAIST 자료가 아니므로 제외. |
| [Suhyoung Choi의 최근 수업](https://mathsci.kaist.ac.kr/~schoi/teaching.html) | 2026 DG·Logic·Lie Groups, 2025 해석다양체·Logic·Differential Geometry 등 공개 페이지는 일정·강의계획 중심이며 실제 영상은 KLMS로 안내. 공개 강의·과제 파일 확보로 계산하지 않았다. |
| [Ilmun Kim 수업](https://ilmunk.github.io/teaching.html) | 2025/2026 수리통계·확률통계 개설 이력만으로 강의 파일·과제 공개를 인정하지 않았다. |
| [Donghwan Kim 수업](https://mathsci.kaist.ac.kr/~donghwankim/teaching.html) | 최신 개설 이력과 과거 강의자료를 구분. 이력 페이지 자체에는 자료 링크가 없어 별도 신규 항목으로 세지 않았다. |
| [금융공학 연구실 수업 목록](https://felab.kaist.ac.kr/courses.html) | IE471 등 개설 이력은 있으나 실제 수업자료·과제 본문은 미확인. |
| [CS101](https://cs101.kaist.ac.kr/) | 직접 요청 응답은 로딩 화면만 반환했고 검색에 잡힌 최신 안내는 Elice 배포. 공개 파일 확보로 계산하지 않았다. |
| [성민혁 교수 과거 수업 목록](https://mhsung.github.io/archive/courses.html) | 2021~2023의 추가 자료 링크도 탐색했지만 이 목록에 넣지 않은 강의는 파일별 접근·분류 검증이 끝나지 않았다. 목록이 없다는 뜻은 아니다. |
| [혼합 학생 보관본](https://github.com/YujunKim02/KAIST_Lectures) | 전체 묶음은 혼합 분류 1개로 포함하되 EPFL 표기 교환수업 AI505/MAS374는 KAIST 정규 개설 과목 수로 계산하지 않았다. |

원문은 [KAIST 데이터](../data/kaist.json)의 항목별 링크를 따른다. 이 저장소는 원문 PDF·노트북·학생 답안이나 개인정보가 담긴 원시 수집물을 미러링하지 않는다. 검색에 드러나지 않는 저장소·교수 홈페이지·과거 학기판은 추가 발견 가능하다.
