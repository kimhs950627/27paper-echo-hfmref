# 27paper-echo-hfmref

EF가 치료 문턱 근처일 때 **재측정이 판정을 바꿀 확률**을 예측하는 연구의 계획·데이터·방법 페이지.

- 사이트: https://kimhs950627.github.io/27paper-echo-hfmref/
- 데이터 리뷰: https://kimhs950627.github.io/27paper-echo-hfmref/review/
- 방법론: https://kimhs950627.github.io/27paper-echo-hfmref/methods/
- 수학 노트: https://kimhs950627.github.io/27paper-echo-hfmref/methods/measurement/

## 한 줄 요약

30일 내 재측정 12,522쌍에서 HFmrEF(40–49) 판정은 **42.5%만 유지**된다.
재분류 여부는 문턱까지 거리 + 비선형 정보로 예측되며(랜덤포레스트 AUC 0.824, 거리 규칙 0.703),
30일과 180일의 문턱 교차율이 **둘 다 17.2%** — 교차가 시간에 누적되지 않으므로 진행이 아니라 측정 불안정이다.

## 데이터 출처

MIMIC-IV-ECHO v1.0.1, MIMIC-IV v3.1 (PhysioNet credentialed).
환자 단위 데이터는 DUA에 따라 공개하지 않으며, 이 저장소에는 **집계 통계만** 있다.

## 구성

| 경로 | 내용 |
|---|---|
| `index.html` | 연구 계획 (질문·근거 3개·모형·임상 경로·한계) |
| `review/index.html` | 데이터 리뷰 (항목 커버리지·EF 구간표기·반복측정 구조·노이즈) |
| `methods/index.html` | 방법론 (잡음 분리·재현율 정의·종점·누수 방지·검증) |
| `methods/measurement/` | 수학 노트 (분산분해·신뢰도·ROC·함정) |
| `methods/msm/` | 구 msm 워크북 → 수학 노트로 리다이렉트 |
| `styles/tokens.css` | 디자인 토큰 (theme: brutalist-poster) |

## 재현

생성기: `src/make_site_reclass.py` (소스 저장소 `27paper-echo`)
수치 원천: `results/pilot_reclass.json`, `results/hfimpef.json`
