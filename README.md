# 정총무 전자 명함 (card.jungchongmoo.com)

프랜차이즈 원스톱 솔루션 **정총무**의 팀원별 디지털 명함. GitHub Pages로 호스팅.

## 명함 3종

| 주소 | 사람 | 전화 | 이메일 |
|---|---|---|---|
| https://card.jungchongmoo.com | 이웅민 대표 | 010-8403-0829 | dndwk0@ |
| https://card.jungchongmoo.com/moon | 문진혁 이사 | 010-2461-0912 | nippert@ |
| https://card.jungchongmoo.com/park | 박웅진 대표 | 010-3800-5086 | woongjin@ |

카카오톡 상담 버튼은 3종 공용 오픈채팅(https://open.kakao.com/o/syDEmKni).

## 구조

```
index.html        이웅민 대표 명함 (루트)
woongmin.vcf      └ 연락처 저장 파일
moon/             문진혁 이사 명함 + jinhyuk.vcf
park/             박웅진 대표 명함 + woongjin.vcf
docs/             사업소개서·견적서 PDF (3종 공용)
og.png            카톡/SNS 미리보기 이미지 (공용)
apple-touch-icon.png  아이폰 홈화면 아이콘 (공용)
CNAME             커스텀 도메인 지정 — 지우면 도메인 끊김!
```

## 수정 방법

- **실적 숫자·문구**: 세 파일(`index.html`, `moon/index.html`, `park/index.html`)에 같은 수정을 반복해야 한다(공용 템플릿 없음 — 단순함 우선).
- **전화·이메일 변경**: 해당 인물 index.html의 `tel:`/`sms:`/`mailto:` 3곳 + "연락처에 저장(...)" 라벨 + 같은 폴더 .vcf 파일까지 5곳.
- **자료 교체**: `docs/`에 같은 파일명으로 덮어쓰고 push — 링크 그대로 유지됨.
- **팀원 추가**: 기존 폴더(예: `park/`) 복사 → 이름·직함·연락처·vcf 수정 → push.
- push 하면 1~2분 내 반영. **CNAME 파일은 절대 삭제 금지.**

## 인프라 메모

- DNS: Spaceship(jungchongmoo.com)에 CNAME `card` → `salescompany0920-afk.github.io`
- HTTPS: GitHub 자동 발급(Let's Encrypt) + enforce ON
- 검증 기준: 3엔진(chromium·webkit·firefox) × 390/768/1280 + 아이폰13·픽셀5 에뮬, 가로 오버플로 0

— 2026-09-02 구축, WM
