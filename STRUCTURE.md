# STRUCTURE — OVENDAYS (오븐데이즈)

울산 동구 방어진 베이커리·디저트 **기본 9.9 브로슈어** 단일 HTML 원페이지.

```
/ (배포 루트, CF [assets] directory="./")
├─ index.html          단일 파일 (인라인 CSS/JS, 모바일 우선)
├─ ov-logo.webp        OVENDAYS 라인 캐릭터 로고 (헤더·파비콘, 원본 206px)
├─ favicon.png         로고 기반 파비콘 (180px)
├─ ov-fruitsand.webp   과일 크림 샌드 (히어로·메뉴01·og)
├─ ov-eggtart.webp     에그타르트 (메뉴02)
├─ ov-bread.webp       오븐 버터 브레드 (메뉴03)
├─ ov-lotus.webp       로투스 크림 샌드 (메뉴04)
├─ ov-peach.webp       백도 복숭아 샌드 (메뉴05)
├─ wrangler.toml       name=ovendays-sample, [assets] ./
├─ .assetsignore       .git·문서·img·_cs 제외
├─ CHANGELOG.md / STRUCTURE.md
└─ img/                원본 105장 (배포 제외)
```

## 섹션 앵커
`#top` 히어로 · `#about` 소개(다크) · `#menu` 시그니처 메뉴(5+더보기) · `#visit` 영업시간+오시는길 · 푸터

## 디자인 (블랙앤화이트 에디토리얼 + 주홍 포인트)
- **팔레트**: 잉크 `--ink #1A1A1A` · 보조 `--ink-soft #565656` · 뮤트 `--muted #666`(AA) · 화이트 `#FFF` · 그레이섹션 `--paper-2 #F3F3F3`(중성 R=G=B) · 라인 `#E4E4E4` · **주홍 `--point #CB3A26`(로고 빨강 기반)** · 텍스트/off용 `--point-deep #A32C1B`.
- **폰트(시안=CDN)**: 영문 디스플레이 **Archivo**(800/900, 워드마크·키커·숫자) + 본문·한글 **Pretendard**. ⚠️납품 시 서브셋 self-host. Pretendard CDN 무버전(CF 이메일난독화 회피).
- 에디토리얼 미니멀: 1px 라인 카드, 각진 버튼(radius 2px), 다크 인트로 대비, tabular-nums 영업시간, 주홍은 포인트에만.
- a11y: reveal + 2.4s 타임아웃 + noscript 폴백, :focus-visible, reduced-motion 폴백, rAF 스무스 앵커(헤더 오프셋 64px).

## 네이버 실데이터 (반영 완료)
- 주소: 울산 동구 방어진순환도로 652 테라스파크 C동 1층 / 올리브영 뒤편.
- 영업: 화·수·목·금·토 12:00–19:00 / **일·월 정기휴무**. 전화 052-201-9807.
- 업종: 울산 다양한 베이커리 디저트집.

## ⚠️ 확인/보류
- **인스타그램 핸들 미확정**(스토어프론트 사진에 "_ovendays" 흔적만) → 링크 미포함. 확인되면 추가.
- 메뉴 가격 미제공 → 사진led, 가격 무표기 + "매장/전화 확인" 안내.
- 네이버 place ID 미확보 → 오시는길 버튼은 네이버 지도 검색 URL(울산 오븐데이즈). place ID 확보 시 교체.
- og:image 상대경로·og:url·canonical = 도메인 확정 후 3줄 동시 추가.
- 폰트 CDN(시안) → 납품 시 self-host. 헤드리스 렌더 미실행(브라우저 다운로드 제한) → 정적 QA 갈음.
