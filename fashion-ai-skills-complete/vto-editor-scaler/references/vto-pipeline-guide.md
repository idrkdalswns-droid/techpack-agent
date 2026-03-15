# 가상 피팅(VTO) 파이프라인 & 배치 양산 상세 가이드

---

## 1. 스타일 누수(Style Bleed) 방어 프로토콜

인컨텍스트 편집의 가장 큰 리스크는 타깃 외 영역이 의도치 않게 변형되는 '스타일 누수'다.

### 보존 방벽 체크리스트

편집 프롬프트 작성 시 반드시 다음 요소의 보존을 명시적으로 선언한다:

| 보존 대상 | 프롬프트 키워드 |
|----------|------------|
| 모델 얼굴 | "Keep facial features, skin tone, expression exactly as original" |
| 포즈/체형 | "Preserve body pose, proportions, and posture" |
| 조명 방향 | "Maintain lighting direction and shadow patterns" |
| 주름 위치 | "Keep fold patterns and wrinkle locations" |
| 배경 | "Do not alter background elements" |
| 색온도 | "Preserve overall color temperature and grading" |

### 실전 예시: 원단 변경

**BAD (보존 방벽 없음):**
```
Change the shirt to a chunky knitted wool.
```
→ 얼굴, 조명, 배경까지 전부 변할 위험

**GOOD (보존 방벽 완비):**
```
Change the fabric of the t-shirt to a heavy, chunky knitted
wool with a cable pattern. Keep the lighting direction, shadows,
folds exactly as they are in the original photo. Do not change
the background, the model's face, skin tone, or body proportions.
Preserve the original color grading and ambient light temperature.
```

---

## 2. 가상 피팅(VTO) 심층 가이드

### 위상수학(Topology) 기반 피팅 원리

단순히 옷을 2D 스티커처럼 오려 붙이는 것이 아니다:

1. **인체 뼈대 역산**: 모델 사진의 골격 구조, 쇄골 돌출, 관절 각도를 3D로 파악
2. **메시 변형**: 의류 원단을 인체 곡선에 맞게 3D로 부풀려 왜곡
3. **조명 재투사**: 원본 스튜디오의 광원 위치에 맞춰 피팅된 의상 위에 그림자/하이라이트 재계산
4. **이질감 제로화**: 원본과 합성 부분의 색온도, 노이즈 그레인, 선명도 통일

### 입력 이미지 품질 요구사항

**모델 사진 (베이스):**
- 해상도: 최소 2000x2000px
- 조명: 균일하고 선명할수록 좋음
- 포즈: 정면 또는 3/4 각도, 팔이 몸통을 가리지 않는 것이 이상적

**의상 사진 (참조):**
- 형태: Flat Lay(평면 컷) 또는 마네킹 착용이 가장 정확
- 배경: 단색 배경이 인식률 최고
- 조명: 고르게 비춰진 상태

### 다중 룩북 스케일링 예시

동일 세션에서 10벌 교체 시 프롬프트 패턴:

```
[1번째] Place the leather jacket from reference onto the model...
[2번째] Now replace with the silk midi dress from reference...
[3번째] Now replace with the navy double-breasted blazer from reference...
```

각 교체마다 반복할 보존 방벽:
```
Preserve the model's face, pose, body proportions, and the
original studio lighting setup. Match shadow density and
color temperature to the original image.
```

---

## 3. 배경 & 조명 재구성 심층 가이드

### 배경 교체 시 환경광 재계산 원칙

새 환경에서 발생하는 빛의 물리적 반사를 피사체에 적용해야 한다.

**올바른 배경 교체:**
```
Place the subject on a snowy mountain terrace.
The cold daylight bouncing off the snow should cast a subtle
blue-white ambient light under the chin and on the coat's lower folds.
The overall color temperature shifts to approximately 6500K.
```

**잘못된 배경 교체:**
```
Put the person on a mountain. (환경광 재계산 없음 → 합성처럼 보임)
```

### 시간대 변경 시 물리적 변환 규칙

단순 컬러 필터가 아니라 태양 고도를 변경하여 그림자를 재계산한다:

| 변환 | 물리적 변화 |
|------|-----------|
| 낮 → Golden Hour | 태양 고도 하강 → 그림자 길어짐 → 색온도 3200K 따뜻해짐 |
| 낮 → 야간 | 직사광 소멸 → 인공 광원 다중 캐스트 → 색온도 혼합 |
| 실내 → 야외 | 인공 조명 제거 → 자연광 방향성 + 환경광 추가 |
| Golden Hour → Blue Hour | 직사광 소멸 → 확산 간접광 → 색온도 7000K+ |

---

## 4. 텍스트 & 로고 통합 심층 가이드

### 오클루전(Occlusion) 마스크 기법

텍스트가 3D 공간 내의 물리적 객체처럼 자연스럽게 녹아들게 한다.

**레벨 1: 기본 텍스트 삽입**
```
Add the text "2026 SUMMER SALE 50%" in clean bold sans-serif
font at the top center of the image. White text with subtle
drop shadow for legibility.
```

**레벨 2: 오클루전 적용 (피사체 뒤)**
```
Place the title text "NOIR COLLECTION" in large elegant serif
font behind the model's head. The model's hair and shoulders
should partially occlude the letters, creating a layered
3D depth effect while maintaining text legibility.
```

**레벨 3: 곡면 매핑 (의류 위)**
```
Render the brand logo "YUKIZ" as embroidered text on the
left chest pocket, following the natural curve and wrinkles
of the fabric. The stitching should show subtle thread texture
and cast micro-shadows consistent with the main lighting.
```

---

## 5. 엔터프라이즈 배치 렌더링 심층 가이드

### API 연동 자동화 아키텍처

```
[PIM/ERP 데이터베이스]
        ↓
  변수 슬롯 자동 채움
  (product_name, garment_spec, background_season, pose)
        ↓
  [히어로 컷 템플릿 × N개 제품]
        ↓
  [나노바나나 프로 API 배치 호출]
        ↓
  [해상도 라우터: 2K WebP / 4K Native 분기]
        ↓
  [CDN 배포 / 인쇄 파일 저장]
```

### 비용 최적화 전략

| 전략 | 방법 | 절감 효과 |
|------|------|---------|
| 해상도 분기 | 웹=2K, 인쇄=4K 분리 발주 | API 크레딧 40~60% 절감 |
| 프롬프트 캐싱 | 동일 세팅 반복 시 변수만 교체 | 프롬프트 설계 시간 90% 절감 |
| 배치 스케줄링 | 비피크 시간대 렌더링 | 처리 속도 향상 |
| QC 자동화 | 첫 10장 수동 확인 → 나머지 자동 | 검수 시간 대폭 절감 |

### 월간 볼륨별 추천 파이프라인

| 월 생성량 | 추천 방식 |
|----------|---------|
| ~50장 | 챗 인터페이스 수동 |
| 50~200장 | 템플릿 + 수동 변수 교체 |
| 200~500장 | API 반자동 (엑셀 변수 연동) |
| 500장+ | 풀 API 자동화 (PIM/ERP 연동) |
