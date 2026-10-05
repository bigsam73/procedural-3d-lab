# procedural-3d-lab

데모씬처럼 **수식으로 계산하는 3D**와 게임 엔진처럼 **저장된 메쉬를 그리는 3D**를 브라우저에서 직접 체감하는 실습 페이지 모음입니다. 라이브러리 없이 WebGL2로만 만들었습니다.

**바로 열기 (GitHub Pages):** https://bigsam73.github.io/procedural-3d-lab/

| 페이지 | 바로 열기 | 소스 | 내용 |
| --- | --- | --- | --- |
| 계산하는 3D, 저장하는 3D | [열기](https://bigsam73.github.io/procedural-3d-lab/compute-vs-store.html) | [`compute-vs-store.html`](compute-vs-store.html) | 같은 장면(사막 위 금속 구)을 왼쪽은 SDF 레이마칭, 오른쪽은 메쉬 래스터라이즈로 나란히 비교. GLSL `map()`을 직접 고쳐 재컴파일할 수 있음 |
| 하이브리드 파이프라인 실험실 | [열기](https://bigsam73.github.io/procedural-3d-lab/hybrid-patterns.html) | [`hybrid-patterns.html`](hybrid-patterns.html) | 하이브리드 패턴 네 가지 실험대: 지형 베이크, 규칙 배치 + 인스턴싱, CPU vs GPU 변형, 고폴리 vs 노멀맵 vs 셰이더 디테일 |
| 듄 런 | [열기](https://bigsam73.github.io/procedural-3d-lab/dune-run.html) | [`dune-run.html`](dune-run.html) | 패턴을 전부 적용한 작은 수집 게임 레벨. 점수판(콤보 · 시간 보너스 · 상위 5개 기록)과 타이머, Web Audio로 합성한 효과음(오디오 파일 0개), 각 요소의 패턴과 디스크 용량 명세표 포함 |
| 학습 노트 | [열기](https://bigsam73.github.io/procedural-3d-lab/study-notes.html) · [PDF](study-notes.pdf) | [`study-notes.md`](study-notes.md) | 세 페이지의 내용을 정리한 학습 노트 |

## 실행

위의 Pages 링크를 열거나, HTML 파일을 브라우저로 직접 열면 됩니다. WebGL2가 필요하며, Chrome 데스크톱에서는 GPU 타이머로 실제 프레임 시간이 표시됩니다.

## 조작

- 캔버스를 끌면 카메라가 돕니다.
- 듄 런: WASD 또는 방향키로 이동, 폰에서는 화면을 끌면 조이스틱, R 키로 다시 시작. 움직이기 시작하면 타이머가 돌고, 수정 하나에 100점, 4초 안에 연속 수집하면 콤보 ×2~×5, 완주 시 시간 보너스 max(0, 600 − 5×초). 상위 5개 기록은 브라우저에 저장됩니다. 효과음은 M 키나 체크박스로 끄고 켤 수 있습니다.
