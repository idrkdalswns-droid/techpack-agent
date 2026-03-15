# 5단계 마스터 프롬프트 공식 및 실전 레시피

나노바나나 프로(Nano Banana Pro)의 추론 모드에 최적화된 구조화된 프롬프트 설계 공식과 주요 아이템별 실전 레시피를 수록한다.

---

## 5단계 마스터 프롬프트 공식 (5-Step Modular Formula)

### 슬롯 ① Context/Role — 컨텍스트 및 역할 부여

AI에게 시각적 기준점과 품질 레벨을 설정한다.

**촬영 목적별 역할 부여 템플릿:**
- 이커머스 상세컷: "Acting as a professional e-commerce product photographer..."
- 에디토리얼 화보: "Acting as a high-end editorial fashion photographer shooting for Vogue..."
- 런웨이 스냅: "Acting as a front-row fashion week photographer capturing runway moments..."
- 브랜드 캠페인: "Acting as an art director for a luxury brand's seasonal campaign..."
- SNS 콘텐츠: "Acting as a lifestyle photographer creating aspirational social media content..."

### 슬롯 ② Core Subject — 주체 및 핵심 묘사

인물과 의류를 세밀하게 서술한다. 반드시 원단 딕셔너리의 물리적 비중 지표를 3개 이상 포함한다.

**구조:**
[인물 묘사] + [의류 구조적 특징] + [원단 물성 키워드 3개+] + [동작/포즈]

**예시:**
"A woman in her late 20s with East Asian features and a neutral expression, wearing an oversized fit heavy gauge cable knit sweater in charcoal grey with a thick turtleneck structure. The knit shows visible cable patterns, structured weight, and gravity-induced drape around the hem."

### 슬롯 ③ Setting/Location — 환경 및 배경

물리적 공간을 묘사하여 반사광과 환경광의 연산 맥락을 제공한다.

**환경 → 광학 효과 매핑:**
| 환경 | 광학 효과 |
|------|---------|
| 비 온 직후 젖은 아스팔트 | 반사광 연산, 네온 반사 |
| 눈 덮인 산/들판 | 차가운 바운스 라이트(cold daylight bounce) |
| 해변/모래사장 | 따뜻한 확산 반사, 수평선 그라데이션 |
| 노출 콘크리트 갤러리 | 부드러운 산란광, 뉴트럴 톤 |
| 네온 가득한 야간 도심 | 다채로운 컬러 캐스트, 강한 콘트라스트 |
| 지중해풍 크림색 건물 거리 | 따뜻한 바운스, 소프트 보케 |

### 슬롯 ④ Style & Technical Specs — 카메라/렌즈/조명

물리적 렌더링의 기준점을 정밀하게 제시한다.

**카메라 기종별 톤:**
| 카메라 | 특성 |
|--------|------|
| Hasselblad X2D | 중형 포맷, 극도의 디테일과 색 깊이 |
| Canon R5 | 풀프레임, 인물 보케 탁월 |
| Leica SL2 | 날카로운 해상도, 시네마틱 색감 |
| Sony A7IV | 범용적, 자연스러운 색감 |

**렌즈별 효과:**
| 렌즈 | 효과 | 용도 |
|------|------|------|
| 24mm 광각 | 공간 왜곡, 배경 과장 | 런웨이, 전신 역동적 샷 |
| 50mm 표준 | 자연스러운 비례 | 범용 화보, 3/4 바디 |
| 85mm f/1.2 | 극도로 얕은 피사계 심도, 크리미 보케 | 인물/의상 집중, 배경 날림 |
| 100mm 매크로 | 1:1 확대, 엣지 투 엣지 선명 | 텍스처 초접사, 디테일 컷 |
| 135mm | 압축 효과, 배경 분리 | 포트레이트, 상반신 |

### 슬롯 ⑤ Constraints & QC — 제약 및 품질 통제

**필수 제약 키워드 (거의 모든 프롬프트에 포함):**
- "No airbrushed look" — 에어브러시 밀어버린 피부 금지
- "visible pores and subtle flaws" — 자연스러운 모공, 미세 결함 유지
- "Authentic film grain" — 필름 카메라 특유의 질감 유지

**상황별 추가 제약:**
- 제품 색상이 중요할 때: "Accurate color rendering under specified lighting"
- 텍스트 포함 시: "Render text with 99% accuracy, no misspelling"
- 로고 포함 시: "Maintain brand logo proportions and placement integrity"

---

## 실전 프롬프트 레시피

### 레시피 1: 클래식 화이트 코튼 셔츠

**설계 핵심:** 면 특유의 무광 마감 + 생활 구김 + 디테일이 날아가지 않는 조명 제어

```
High-resolution studio editorial photo of a male model wearing a crisp white
cotton shirt. The shirt has a natural matte finish and subtle texture variations.
Show the visible weave structure in areas where the soft directional light rakes
across the surface. The fit is slightly oversized, displaying light natural wrinkles
and gravity-induced drape around the rolled sleeves and open collar. Ensure the
fabric interacts intimately with the body, showing subtle drag lines to indicate
tension. No airbrushed look; the model's skin must show natural texture, visible
pores, and subtle flaws for absolute photorealism. Shot on Hasselblad X2D 135mm
at f/5.6. Neutral gray seamless backdrop with gentle falloff. Clean, bright cinematic
color grading with balanced tones.
```

**설계 의도 분석:**
- `natural matte finish` → 스페큘러 반사 억제, 난반사 위주 렌더링
- `visible weave structure... light rakes across` → 측면광이 원사 짜임새에 만드는 마이크로 텍스처 그림자
- `gravity-induced drape` + `drag lines` → 2D 스티커가 아닌 3D 물리적 의류 인식
- `No airbrushed look` + `visible pores` → 불쾌한 골짜기 차단

### 레시피 2: 더스트 로즈 썸머 원피스

**설계 핵심:** 경량 원단의 공기역학적 움직임 + 빛 투과 + 골든아워 감성

```
A hyper-realistic cinematic portrait of a woman walking confidently outdoors
wearing a flowing dust rose linen-blend summer dress. The dress features
gentle natural folds, reacting to a slight breeze with liquid motion and a
fluttering hem. The fabric tension shows distinct drag lines around the waist
where it is subtly cinched, while the skirt balloons lightly to show a breathable
weave. Lighting is warm natural sunlight during Golden Hour, creating crisp
shadows, soft internal light reflections, and golden highlights on the textured
fabric. Shot from a slightly low angle on a 50mm f/2.0 lens with a shallow depth of
field. Soft bokeh background of a Mediterranean street with cream buildings.
Authentic film grain, high dynamic range, photorealistic.
```

**설계 의도 분석:**
- `flowing, liquid motion, fluttering` → 경량 소재 인식, 공기역학 반응
- `drag lines around the waist` + `balloons lightly` → 조여진 허리 vs 펼쳐진 스커트 대비
- `soft internal light reflections` → 얇은 원단의 빛 투과(Subsurface Scattering) 시뮬레이션
- `Golden Hour` + `authentic film grain` → 필름 카메라 감성 노이즈

### 레시피 3: 데님 재킷 스트리트 화보

**설계 핵심:** 중량 원단의 구조적 무게감 + 도시 반사광 + 스트리트 역동성

```
Street-style editorial photograph of a young man wearing a raw indigo denim
jacket with visible creasing at the elbows, rigid structure maintaining its shape,
and gravity-induced drape pulling the hem downward. Heavy brass buttons catch
light with sharp metallic reflections. The denim shows deep twill weave texture
with subtle fading at stress points. The model walks through a rain-soaked Tokyo
alley at night, neon signs reflecting off wet asphalt creating colorful light pools.
Shot on Leica SL2 with 35mm lens at f/2.8. Shallow depth of field isolating the
subject. Kodak Portra 400 film emulation with warm undertones and natural grain.
No artificial smoothing on skin or fabric textures.
```

---

## JSON 슈도코드 출력 템플릿

변수를 분리 선언하여, 이후 특정 변수만 교체하면 시리즈 이미지를 양산할 수 있다.

```json
{
  "SUBJECT_IDENTITY": "30대 초반 아시아계 여성, 뉴트럴 표정, 자연스러운 피부결",
  "GARMENT_SPEC": "오버사이즈 헤비 게이지 케이블 니트, 차콜 그레이, 두꺼운 터틀넥",
  "FABRIC_PHYSICS": ["structured weight", "gravity-induced drape", "visible cable patterns"],
  "ENVIRONMENT_SCENE": "노출 콘크리트 갤러리, 커다란 창으로 들어오는 부드러운 산란광",
  "CAMERA_PHYSICS": "Hasselblad X2D 135mm, f/5.6, 얕은 피사계 심도",
  "LIGHTING_RIG": "하이키 상업 조명, 우측 상단 메인 소프트박스, 좌측 반사판",
  "CONSTRAINTS": ["No airbrushed look", "visible pores", "authentic film grain"]
}
```

→ RENDER: 위 변수를 엄격하게 적용하여 4K 해상도의 패션 룩북 이미지를 렌더링하라.
