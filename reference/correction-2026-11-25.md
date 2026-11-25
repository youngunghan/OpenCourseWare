# 정정 기록 — 2026-11-25

> 범위: [2026-11-06 게시본 재검토](recheck-2026-11-06.md)가 지적한 두 문제, KAIST-K004의 학기 원본 표기와 SNU-C005의 접근 상태 기록을 정정한다. 원본 파일 바이트는 바꾸지 않았고 새 원본도 추가하지 않았다. 이 문서는 정정 내용과 근거를 남기는 기록이며 독립 검토가 끝났다는 표시가 아니다. 로그인 강의실, 영상 재생, 원본 코드 실행은 범위 밖이다.

[첫 화면](../README.md) · [전체 보관 상태](../catalog/originals.md) · [이전 재검토](recheck-2026-11-06.md)

## 1. KAIST-K004: 학기 원본 미확인으로 분리 (보고서 수정안 중 첫 번째 안)

재검토 보고서는 두 가지 수정안을 제시했다. 하나는 K004를 학기 원본 미확인으로 분리하고 G001/G002를 관련 현재 자료로 연결하는 것이고, 다른 하나는 2025 당시 커밋을 따로 확인해 보관하는 것이다. 이번에는 **첫 번째 안**을 택했다. 두 번째 안은 원본 추가를 뜻하므로 이번 정정 범위 밖이다.

근거는 보관본 자체다. 보관한 NeRF README는 수업을 2026 Spring, 마감을 2026-04-28로 표기한다. PointNet README는 2026 봄 수업 페이지(kaist-cs479-spring-2026)를 연결한다. PointNet LICENSE에는 2023 Fall 과제 표기가 남아 있다. 이 저장소의 해당 파일을 직접 대조해 확인했다. 이 표기들은 서로 다른 시점의 고지이고, 2025 봄 수업이 실제 배포한 판본을 알려 주지 않는다. 반대로 LICENSE의 2023 표기만으로 다른 학기(예: K007)의 전체 파일이 확보됐다고 추정하지도 않는다.

### 스키마 추가: `related_current_material`

`reference/original-coverage.json`의 status에 새 값 `related_current_material`을 추가했다. 연결한 소스가 해당 학기의 당시 배포본으로 확인되지 않은 현재 자료일 때 쓰며, 학기별 원본 보관으로 세지 않는다. 보관된 파일과 ID 연결은 그대로 둔다. 현재 이 값을 가진 항목은 KAIST-K004 하나다. 값의 정의는 [methodology.md](methodology.md)에 기록했다. `status_counts`에는 0개인 `access_and_permission_unconfirmed`도 어휘 보존을 위해 남겼다.

### `course_ids`를 고치지 않은 이유

`reference/original-files.json`의 G001/G002와 `reference/original-rights-audit.json`의 NeRF·PointNet 항목은 `course_ids`에 KAIST-K004를 계속 포함한다. 의도한 것이다. 이 파일들은 K004 수업이 연결한 저장소의 현재 자료이며 "관련 자료"라는 연결 자체는 사실이다. 달라진 것은 그 연결을 학기 원본 보관으로 세지 않는다는 점이고, 그 판단은 coverage 쪽 status가 담당한다. 따라서 두 파일은 수정하지 않았다. `materials/README.md`와 두 ORIGINAL-SOURCE.md에는 K004 연결이 관련 현재 자료라는 날짜 있는 안내만 추가했다.

### 집계 변화

| 항목 | 정정 전 | 정정 후 |
| --- | --- | --- |
| 일부 원본(stored_partial) | 14 | 13 |
| 학기 원본 미확인(related_current_material) | 0 | 1 |
| 미보관·학기 원본 미확인을 합친 나머지 | 203 | 204 |
| KAIST의 일부 원본 있는 항목 | 4 | 3 |
| permission_unconfirmed | 179 | 180 |
| access_and_permission_unconfirmed | 1 | 0 |

서울대 5개, POSTECH 5개는 그대로다. 서울대 5개 중 Software Foundations 3개 항목(SNU-C003·C021·C046)은 학기 당시 판본이 아니라 현재 교재 배포본을 일부 원본으로 센다. 이 사실은 `catalog/originals.md`에 문장으로 명시했고 집계 방식은 바꾸지 않았다.

## 2. SNU-C005: 페이지와 PDF의 접근 상태 분리

2026-11-25에 로그인 없이 읽기 전용 HTTP 요청으로 두 대상을 따로 확인했다. 대상별로 최대 3회, 간격 60초, 요청 제한 30초이며 성공하면 그 대상은 멈춘다. HTTPS만 시도했고 HTTP 대안은 시도하지 않았다. 대상 A는 진입 페이지 `https://datalab.snu.ac.kr/~ukang/courses/26F-DS/`, 대상 B는 그 하위의 `L1-intro.pdf`다.

성공 기준은 다음과 같다. A는 HTTPS 2xx이면서 본문에 "2026"·"Fall 2026"·"26F" 중 하나와 "자료구조"·"Data Structure"·"Data Structures" 중 하나가 있는 것이다. B는 2xx 응답(이번 응답은 206)이면서 본문이 `%PDF`로 시작하는 것이다. B는 64KiB 범위 요청(`Range: bytes=0-65535`)이다.

### 원시 결과

| 시각(UTC / KST) | 대상·회차 | 상태·오류 | 바이트 | 판정 |
| --- | --- | --- | ---: | --- |
| 2026-11-25 04:24:26Z / 13:24:26 | A · 시도 1 | 오류: 연결이 원격 호스트에 의해 강제로 끊김(WinError 10054, 0.1초) | 0 | 실패 |
| 2026-11-25 04:25:26Z / 13:25:26 | A · 시도 2 | HTTP 200, `text/html`, 제목 "Fall 2026, M1522.000900 Data Structur…" | 9,089 | 성공: "2026"·"Fall 2026"과 "Data Structure(s)" 포함 |
| 2026-11-25 04:25:26Z / 13:25:26 | B · 시도 1 | HTTP 206, `application/pdf`, Content-Range `bytes 0-65535/182083` | 65,536 | 성공: `%PDF` 시작 |

적용한 분기는 **A 성공**이다. 판정 규칙은 A만으로 상태를 정한다. 따라서 coverage status는 `access_and_permission_unconfirmed`에서 `permission_unconfirmed`로 바뀌었다. `access_state`와 coverage `reason`은 페이지 문장과 PDF 문장을 각각 자기 대상의 결과에서 만들었다. 수업 페이지 접속 확인(2026-11-25), 소개 PDF(L1-intro.pdf) 접속 확인(2026-11-25), 재배포 허가 미확인이다. 세 시도는 모두 `evidence[]`에 추가했고 기존 2026-11-03·11-04 항목은 그대로 두었다. 2026-11-06 재검토의 결과(진입 페이지 연결 실패, PDF 206)도 보고서 기록에 따라 날짜를 붙여 추가했다.

이 결과가 뜻하는 것은 이 호스트에서 이 시점에 접속이 됐다는 것뿐이다. 같은 페이지가 11-06에는 연결이 끊겼고 11-25 첫 시도에서도 끊겼다가 1분 뒤 성공했으므로 접속 상태는 시점에 따라 달라진다. 접속 성공은 재배포 허가를 뜻하지 않으며, PDF는 앞 64KiB 표본만 확인했다.

## 3. 변경한 파일

- 데이터: `data/kaist.json`(K004), `data/snu.json`(C005)
- 보관 상태: `reference/original-coverage.json`, `catalog/originals.md`
- 설명: `README.md`, `reference/methodology.md`, `reference/original-intake.md`, `reference/correction-2026-11-25.md`(이 문서)
- 카탈로그 보기: 열 개의 보기를 JSON 정본에서 다시 생성했고 `catalog/kaist.md`의 K004 절과 `catalog/snu.md`의 C005 절만 달라졌다. 나머지 여덟 개는 바이트까지 같다. 집계 줄도 달라지지 않았다. 확인일은 두 항목 모두 JSON의 `checked_date`(2026-11-04)를 유지했고, 이번 확인일은 `access_state`와 `evidence[]`에 날짜로 남겼다.
- 원본 폴더: `materials/README.md`와 G001·G002의 `ORIGINAL-SOURCE.md` 두 개에 안내 문장만 추가했다. 원본 파일의 바이트는 바꾸지 않았다.

## 4. 남은 한계

- 이전의 날짜 있는 보고서(`recheck-2026-11-04.md`, `recheck-2026-11-06.md/json`)는 당시 기록이므로 고치지 않았다. 옛 집계와 옛 상태가 그대로 남아 있다.
- `reference/snu-provenance.md`의 "2026-11-04 재검토에서는 네 항목 모두 페이지·PDF 재접속에 성공했다"는 문장은 그날의 사실이므로 그대로 두었다. 11-06·11-25 결과는 이 문서와 JSON 정본에 있다.
- `reference/original-coverage.json`의 최상위 `checked_date`는 2026-11-04로 남겼다. 정정한 두 항목의 날짜는 각 `reason`과 JSON 정본의 `evidence[]`에 있다.
- `build_originals_metadata.py`는 실행하지 않았다. `catalog/originals.md`, `materials/README.md`, 두 ORIGINAL-SOURCE.md, coverage JSON은 손으로 고쳤다. 그 스크립트를 이후 다시 돌리면 옛 상태 값과 옛 집계로 이 정정을 덮어쓸 수 있으므로, 돌리기 전에 `related_current_material`을 알도록 고쳐야 한다.
- 이번 접속 확인은 이 호스트 한 곳, 한 시점, HTTPS 한 경로의 결과다. 다른 네트워크나 다른 시각의 결과를 보장하지 않는다.
- K004의 2025 봄 당시 배포본을 확인하거나 보관하는 두 번째 안은 하지 않았다. 별도 작업이다.

## 5. 검증

정정 뒤 아래를 실행했다. 명령과 원문 출력은 이 정정을 넘겨받는 보고에 따로 남긴다.

- 바뀐 JSON 세 개(`data/kaist.json`, `data/snu.json`, `reference/original-coverage.json`)가 모두 파싱된다.
- `git diff --stat -- materials/`가 `materials/README.md`와 두 ORIGINAL-SOURCE.md만 보이며 `git diff --numstat`에 이진 변경(`-`)이 없다.
- 일관성 검사: `status_counts`가 records의 상태별 개수와 같고, `catalog/originals.md`의 상태 열이 모든 ID에서 coverage status와 같으며, README·intake·methodology·originals.md의 집계가 `status_counts`에서 나온 13/204와 같다. C005의 status와 `reason`의 두 문장이 위 원시 결과와 맞고, 증거 항목이 시도마다 하나씩 있다.
- 카탈로그 구조 검사(`check_views.py`)가 통과한다.
