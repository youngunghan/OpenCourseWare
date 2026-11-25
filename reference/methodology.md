# 분류·데이터 필드

[첫 화면](../README.md) · [갱신 방법](../CONTRIBUTING.md)

## 분류

| 값 | 의미 |
| --- | --- |
| `both` | 일부 강의/실습/녹화와 일부 과제 자료가 함께 확인됨. 해설·프로젝트 지침만 있는 경우도 과제 형태에 표시. |
| `lecture` | 강의 측만 확인. 과제 미확인은 과제가 없다는 뜻이 아님. |
| `assignment` | 과제 측만 확인. 학생 구현만 있는 경우도 있어 출처·형태 확인 필요. |
| `mixed` | 여러 학기·과목 혼합 보관본. `both` 등에 중복 집계하지 않음. |
| `info` | 안내·참고·평가 정보이거나 실제 자료 본문·현재 접근 미확인. 자료 확보로 계산하지 않음. |

‘확인’은 항목에 적은 수준의 확인이다. 공식 페이지의 공개 자료 링크, PDF/노트북 본문 표본, 저장소 파일 목록은 서로 다른 증거 수준이다. 전체 파일 다운로드·영상 재생·프로그램 실행·정답성·전체 학기 완전성은 별도다. `full_semester_verified`는 현재 전부 `false`다.

## 주요 필드

| 필드 | 의미 |
| --- | --- |
| `id`, `school` | 안정 ID와 학교. 과목 수 대신 자료 진입점을 식별. |
| `department`, `course`, `provider`, `source_kind` | 실제 개설·관련 학과, 수업명, 제공자, 공식/학생 등 출처 유형. |
| `term`, `year`, `semester` | 표시 학기와 정렬값. 봄 1, 가을 2; 원본에 다른 학기값이 있으면 그 값을 보존. 학기 미상·혼합은 `null`. 추정·충돌은 표시·근거 보존. |
| `classification`, `classification_label` | 분류 값과 표시명. |
| `lecture_confirmed`, `assignment_material_confirmed` | 자료 측 확인 플래그. SNU 혼합 자료는 양쪽이 `true`여도 분류는 `mixed`; KAIST·POSTECH 혼합은 양쪽을 단일 학기로 확정하지 않아 `false`를 사용. `mixed`에서는 `false`가 해당 파일이 없다는 뜻이 아니므로 링크·비고를 우선. |
| `lecture_links`, `assignment_links` | 이름·원문 URL 배열. 본문 파일 또는 명시된 자료 목록 링크. |
| `assignment_forms` | `problem` 실제 문제/지정 연습, `skeleton` 코드 뼈대, `student` 학생 풀이·구현, `solution` 과제 해설, `project_brief` 프로젝트 수행 지침, `mixed` 혼합. 해설의 공식성은 출처 유형·비고로 확인. |
| `unavailable_links` | 404·인증/쿠키 요구·본문 파싱 실패 등으로 현재 자료 링크에서 분리한 원문 URL과 사유·확인일. URL을 지우거나 삭제/비공개라고 단정하지 않음. |
| `checked_date`, `access_state`, `evidence` | 확인 날짜, 접근·검증 한계, 근거 URL·검토 종류·결과. 서울대 이전일은 재다운로드 날짜가 아님. |
| `classification_reason`, `notes` | 분류 이유, 학기 추정·오표기·접근 실패·부분 공개 등 제한. |

## 범위와 증거

서울대 124개는 최초 이전 시 원문·분류를 보존했고, 2026-11-04 재검토에서 현재 접근·본문 근거에 따라 일부 분류와 링크를 수정했다. KAIST 56개는 공개 수업 페이지·저장소 파일 목록과 실제 자료 표본을 확인해 추가했다. POSTECH 37개는 2026-11-04 공개 수업 페이지·학생 보관본·대표 파일 본문을 확인해 추가했다. 세 학교의 자료 수집일과 검증 깊이는 같지 않다. 재배포 범위를 확인한 원본은 materials/에 보관하며 [원본 목록](../catalog/originals.md)에 상태를 표시한다. 조사 중간 파일·검수 프롬프트·우리 머신/위키 경로·쿠키·토큰은 공개 저장소에 보관하지 않는다.

검색되지 않는 공개 자료, 삭제된 자료, 외부 저장소 이름 변경, 교수 이동, LMS 전용 자료 등으로 누락이 있을 수 있다. 제외·미확인 후보를 [KAIST 조사 기록](kaist-research.md)과 [POSTECH 조사 기록](postech-research.md)에 남겼다. eTL 및 기타 비공개 강의실의 자료는 이 목록 범위 밖이다.

## 공개 원문과 저장된 원본의 차이

기존217개 항목의 확인 플래그는 원출처 공개 자료의 존재 판단이며 이 저장소의 원본 보관 여부와 다르다. ID·학기·분류·완비 플래그는 변경하지 않았다.

reference/original-files.json은 원본 541개의 출처·경로·크기·SHA-256·고정 Git blob·조건의 정본이다. 경로는 source.root와 file.source_path를 합친다. files[].license와 파일 내부/중첩/추가 용도 조건을 우선한다. upstream_attributions에는 원출처·고정 버전·확인한 라이선스·고지 사본을 기록한다. 단순 알고리즘/매개변수 참고도 있어 모든 참조가 파일 전체의 복제를 뜻하지 않는다.

출처 기록37개 중 원본이 있는33개와 원본0개 조사 기록4개를 status/files로 구분한다. reference/original-coverage.json은 일부 원본13개와 나머지204개(미보관 또는 학기 원본 미확인)의 사유를 구분한다. reference/original-excluded-files.json은 처음 조사한17개 GitHub 범위의 미보관 1248개 경로와 Gitblob, 알려진 SHA256을 기록한다. reason은 reason_definitions의 사유 코드이며 reason_counts는 그 집계다. 전 세계 파일의 목록이나 재배포 금지 확정을 뜻하지 않는다.

reference/original-coverage.json의 status 값은 stored_partial(허용 범위가 확인된 일부 원본 보관. Software Foundations 3개 항목(SNU-C003·C021·C046)은 학기 당시 판본이 아니라 현재 교재 배포본을 일부 원본으로 센다), related_current_material(2026-11-25 추가: 연결한 소스가 해당 학기 당시 배포본으로 확인되지 않은 현재 자료이며 학기별 원본 보관으로 세지 않음. 보관된 파일은 그대로 두고 연결만 유지하며 현재 KAIST-K004 1개), permission_unconfirmed(공개 접근·원출처 링크는 있으나 재배포 허용 범위 미확인), license_scope_unconfirmed(라이선스 적용 범위가 불명확하거나 충돌), no_verified_material_in_catalog(실제 자료 미확인), access_and_permission_unconfirmed(접근 오류와 허가 미확인을 함께 기록하는 값, 현재 0개), restricted_terms(이용 범위 제한)다. status_counts는 records의 상태별 개수와 일치해야 하며 0개인 값도 어휘 보존을 위해 남긴다. related_current_material은 stored_partial 집계에 넣지 않으므로 일부 원본 13개와 나머지 204개를 합해 217개다. 정정 경위는 correction-2026-11-25.md에 있다.

학생 보고서의 이름·학번을 함께 담은 main.tex 원본8개는 공개 보관에서 제외했다. 원본 표지를 편집하지 않았으며 나머지 본문 조각·서지·루트 고지는 부분 보관이다. 문서 컴파일·보고서 완비는 보장하지 않는다. 파일별 제외 목록에 개인정보 사유를 기록했다.

제외 목록의 source_path_redacted=true 항목은 공개 원출처 파일명에 있는 학번 부분을 [student-number]로 바꾼 표시 경로다. 원래 UTF-8 경로의 SHA256과 파일 Gitblob/SHA256은 유지한다. 가명 경로는 다운로드 경로가 아니며, 원본 파일의 바이트를 바꾼 것이 아니다. 원래 경로는 공개 저장소 밖 로컬 감사 근거에만 보관한다.
