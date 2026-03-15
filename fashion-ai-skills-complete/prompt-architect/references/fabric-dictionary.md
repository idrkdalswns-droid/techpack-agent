# 원단 딕셔너리 (Fabric Dictionary) — 물리적 비중 지표 매핑 테이블

나노바나나 프로의 추론 엔진에게 원단의 물성을 정확히 인지시키기 위한 산업 전문 어휘(Industry Vocabulary) 매핑 테이블이다. 추상적인 형용사 대신 직물의 물리적 특성을 대변하는 키워드를 사용해야 한다.

---

## 1. 직물 저항성과 무게감 (Weight & Resistance) 매핑

### 저항성 낮음 / 경량 직물

| 원단 | 한국어 설명 | 필수 삽입 키워드 |
|------|----------|---------------|
| 실크 (Silk) | 가볍고 유려하게 흐름 | fluttering, liquid motion, cascading, smooth sheen |
| 시폰 (Chiffon) | 투명하고 바람에 나부낌 | billowing, translucent layers, floating, ethereal movement |
| 새틴 (Satin) | 광택이 강하고 흐르는 듯함 | liquid drape, high sheen surface, cascading folds, reflective |
| 거즈 (Gauze) | 투명하고 성기게 짜여짐 | breathable weave, light-permeable, airy texture, delicate layering |
| 저지 (Jersey) | 가볍고 신축성 있음 | soft stretch, body-conforming, gentle cling, relaxed drape |

**공기역학적 동적 키워드 풀:**
fluttering(가볍게 나부끼는), cascading(폭포수처럼 떨어지는), billowing(바람에 부풀어 오르는), liquid motion(액체가 흐르는 듯한 움직임), floating(부유하는), ethereal(공기처럼 가벼운)

### 저항성 높음 / 중량 직물

| 원단 | 한국어 설명 | 필수 삽입 키워드 |
|------|----------|---------------|
| 데님 (Denim) | 단단하고 뻣뻣한 능직 | creasing, rigid structure, gravity-induced drape, stiff folds |
| 가죽 (Leather) | 무겁고 광택/마모 공존 | sagging, rigid, structured, heavy weight distribution |
| 두꺼운 울 (Heavy Wool) | 묵직하고 형태 유지 | gravity-induced drape, structured silhouette, bulky texture |
| 캔버스 (Canvas) | 거칠고 단단함 | coarse texture, rigid surface, minimal drape, raw stiffness |
| 트위드 (Tweed) | 두껍고 직조 패턴 뚜렷 | textured surface, woven pattern visible, structured weight |
| 코듀로이 (Corduroy) | 골이 깊고 무게감 있음 | ribbed texture, deep grooves, structured drape |

**무게감 정적 키워드 풀:**
creasing(굵고 깊게 패인 주름), sagging(무게를 이기지 못하고 처지는), rigid(구조적으로 뻣뻣한), structured(구조적인), gravity-induced drape(중력에 의한 묵직한 처짐)

---

## 2. 마찰과 장력 (Tension & Friction) 키워드

인체와 의류가 상호작용하는 지점에서 발생하는 물리적 현상을 묘사하는 키워드. "옷이 몸 위에 덧그려진 2D 스티커처럼 보이는(Painted-on look)" 현상을 박살내는 핵심 기술이다.

| 상황 | 키워드 | 설명 |
|------|--------|------|
| 옷이 당겨지는 곳 | drag lines | 장력에 의해 원단이 당겨지며 생기는 빗살 무늬 주름 |
| 솔기에 힘이 가해지는 곳 | seam stress | 솔기 부분 박음질에 가해지는 텐션 |
| 허리가 조여진 곳 | cinched waist tension | 벨트/코르셋으로 좁게 조여진 부위의 압력 |
| 관절이 구부러진 곳 | joint compression folds | 팔꿈치/무릎 굽힘에 의한 주름 |
| 옷이 헐렁한 곳 | gravity pull, loose drape | 중력에 의해 자연스럽게 처지는 여유분 |

**사용 예시:**
"The fabric tension shows distinct drag lines around the waist where it is subtly cinched, while the skirt balloons lightly to show a breathable weave."

---

## 3. 표면 마감 및 빛 반사율 (Surface & Light Interaction) 매핑

### 면(Cotton) / 리넨(Linen) — 난반사(Diffuse Reflection) 계열

| 키워드 | 효과 |
|--------|------|
| natural matte finish | 무광 마감, 스페큘러 반사 억제 |
| visible weave structure when light rakes across | 측면광에 드러나는 미세 원사 교차 구조 |
| rough paper fibers | 거친 종이 같은 섬유질 |
| organic stiffness | 유기적인 뻣뻣함 |
| subtle texture variations | 미세한 텍스처 변주 |

### 가죽(Leather) / 합성 피혁 — 혼합 반사 계열

| 키워드 | 효과 |
|--------|------|
| high gloss surfaces | 고광택 표면 |
| sharp reflections | 날카로운 빛 반사 |
| worn matte patches | 오랜 사용으로 광택이 죽은 부위 |
| subtle scratches | 미세한 스크래치 |
| visible pores and stitch detail | 눈에 띄는 모공과 스티치 디테일 |

### 실크(Silk) / 새틴(Satin) — 정반사(Specular Reflection) 계열

| 키워드 | 효과 |
|--------|------|
| smooth kicker | 부드러운 킥 라이트 |
| distinct reflection patterns | 뚜렷한 반사 패턴 |
| mirror-like quality | 거울같은 광택 |
| intense highlights | 강렬한 하이라이트 |

---

## 4. 빛의 투과 (Subsurface Scattering) 키워드

얇은 원단(시폰, 리넨, 거즈)을 통과하는 빛의 산란 효과를 시뮬레이션하기 위한 키워드.

| 키워드 | 효과 |
|--------|------|
| soft internal light reflections | 원단 내부에서 부드럽게 반사되는 빛 |
| light passing through the weave | 직조 사이를 투과하는 빛 |
| breathable weave revealing backlighting | 통기성 짜임새 사이로 드러나는 역광 |
| translucent fabric glow | 반투명 원단의 은은한 광채 |

**사용 시점:** 여름용 시폰/리넨 원피스, 역광(backlighting) 환경, 야외 자연광 촬영 시 필수 삽입
