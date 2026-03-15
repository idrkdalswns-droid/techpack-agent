# 상업 패션 조명 & 카메라 광학 세팅 가이드

나노바나나 프로의 추론 엔진이 연산할 수 있는 상업 패션 촬영의 물리적 파라미터 가이드.

---

## 1. 조명 기법 상세 스펙

### High-key 상업 조명 (이커머스/카탈로그)

**목적:** 제품의 디테일과 색상을 왜곡 없이 선명하게 보여줌

**프롬프트 구문:**
```
High-key commercial lighting. Large softbox source overhead.
White bounce cards filling shadows. Even, flattering illumination.
```

**물리적 세팅:**
- 메인 광원: 머리 위 대형 소프트박스 (120cm+)
- 보조: 좌우 화이트 반사판으로 그림자 채움
- 배경: 순백(#FFFFFF) 또는 뉴트럴 그레이
- 결과: 균일하고 화사한 조도, 그림자 최소화

### Rembrandt 에디토리얼 조명 (화보/에디토리얼)

**목적:** 텍스처 입체감과 극적인 무드 강조

**프롬프트 구문:**
```
Classic Rembrandt lighting. Key light at 45 degrees elevation.
Triangle of light on the shadowed cheek. Deep shadow density.
```

**물리적 세팅:**
- 메인 광원: 45도 상단 1개 (약 2m 높이)
- 모델 뺨에 역삼각형 빛 패턴 형성
- 그림자 밀도 높음 → 극적 대비
- 선택: Kodak Portra 400 필름 에뮬레이션으로 따뜻한 톤

### 자연광 세팅 (아웃도어)

**Golden Hour (해 질 녘):**
```
Warm natural sunlight during Golden Hour. Low sun angle creating
long dramatic shadows. Golden highlights on textured fabric.
Soft warm color temperature around 3200K.
```

**Blue Hour (해 뜨기 직전/직후):**
```
Cool ambient light during Blue Hour. Soft diffused illumination
with blue-purple color cast. No harsh shadows. Ethereal mood.
```

**정오 직사광 (드라마틱):**
```
Harsh midday sun creating strong contrast. Deep black shadows
under chin and collar. Bright specular highlights on fabric surface.
```

### 매크로/디테일 조명

**프롬프트 구문:**
```
10ft Octabank, camera left, 50% power. Ring light fill, on-axis.
Even illumination revealing micro-texture details.
```

---

## 2. 렌즈 & 광학 시뮬레이션 상세 가이드

### 24mm 광각 (Wide Angle)

**프롬프트 구문:**
```
Shot on Leica SL2 with a 24mm lens. Exaggerate foreground features.
Wide perspective distortion emphasizing spatial depth.
```

**효과:** 공간 왜곡, 배경과 인물 비례 과장, 역동적 에너지
**용도:** 런웨이, 전신 스트리트 스냅, 공간감 강조

### 50mm 표준 (Standard)

**프롬프트 구문:**
```
Shot on Sony A7IV with 50mm f/2.0 lens. Natural perspective
with minimal distortion. Moderate depth of field.
```

**효과:** 인간의 눈과 가장 유사한 자연스러운 비례
**용도:** 범용 화보, 3/4 바디, 일상적 스타일링

### 85mm 인물 (Portrait)

**프롬프트 구문:**
```
Shot on Canon R5 with 85mm f/1.2 lens. Extremely shallow
depth of field. Bokeh should be creamy and circular.
```

**효과:** 배경 완전 날림, 모델과 의상에 시선 집중
**용도:** 포트레이트, 상반신 화보, 의상 디테일 강조

### 135mm 망원 (Telephoto)

**프롬프트 구문:**
```
Shot on Hasselblad X2D with 135mm lens at f/5.6.
Compressed perspective separating subject from background.
```

**효과:** 배경 압축, 인물 분리, 깊이감 있는 포트레이트
**용도:** 클래식 패션 화보, 격식 있는 룩북

### 100mm 매크로 (Macro Close-up)

**프롬프트 구문:**
```
100mm Macro lens. 1:1 magnification. Focus stacking simulation
for edge-to-edge sharpness on the product texture.
```

**효과:** 지퍼, 박음질, 원단 올 등 마이크로 텍스처 극대 확대
**용도:** 제품 디테일 컷, 소재 QC, 텍스처 홍보

---

## 3. 촬영 목적별 통합 세팅 매트릭스

### 이커머스 상세 컷
```
Camera: Phase One XF, 80mm lens, f/7.2
Lighting: High-key, large softbox overhead, white bounce cards
Background: Pure white seamless
Output: 2000x2000px, 1:1 ratio, 72-150 DPI, WebP
Keywords: Even illumination, flattering light, product-focused
```

### 에디토리얼 화보
```
Camera: Hasselblad X2D, 135mm, f/5.6
Lighting: Classic Rembrandt or three-point
Background: Contextual (location-based)
Output: Native 4K, 16:9 or 3:4 ratio
Keywords: Deep shadows, dramatic contrast, film grain
Film: Kodak Portra 400 emulation
```

### 런웨이 스냅
```
Camera: Leica SL2, 24mm, f/2.8
Lighting: Mixed venue lighting with flash
Background: Runway with audience blur
Output: Native 4K, 2:3 ratio
Keywords: Dynamic motion, energy, front-row perspective
```

### SNS 캠페인
```
Camera: Sony A7IV, 35mm, f/2.0
Lighting: Natural or mixed ambient
Background: Lifestyle context (café, street, park)
Output: 1080x1350px (4:5 ratio) for Instagram
Keywords: Aspirational, lifestyle, candid feel
```

### 텍스처/디테일 매크로
```
Camera: Any + 100mm Macro
Lighting: Ring light + Octabank
Background: Neutral or fabric-matched
Output: Native 4K, 1:1 ratio
Keywords: Edge-to-edge sharpness, focus stacking, micro-detail
```

---

## 4. 추론 모드 물리 연산 체크리스트

이미지 렌더링 전 반드시 확인해야 할 물리적 타당성:

1. **그림자 방향**: 광원 위치와 그림자 캐스팅 방향이 일치하는가?
2. **그림자 길이**: 태양 고도(시간대)에 맞는 그림자 길이인가?
3. **환경광 반사**: 주변 물체(눈, 물, 벽)의 색온도가 피사체에 반영되었는가?
4. **원단 투과**: 얇은 원단에 빛이 통과하는 Subsurface Scattering이 적용되었는가?
5. **중력 vs 장력**: 헐렁한 부위는 처지고, 팽팽한 부위는 당겨지는 물리적 대조가 있는가?
6. **보케 품질**: 렌즈 조리개에 맞는 보케 형태(원형/다각형)인가?
