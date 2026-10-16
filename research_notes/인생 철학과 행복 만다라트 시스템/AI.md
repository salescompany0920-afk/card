# AI 테마 — 1인 소상공인(가맹 영업 대행·점포 개발·인테리어 + 신발 + 메디쏠라)의 AI 활용 조사 노트

조사일: 2026-10-16. 범위: 만다라트 "AI" 테마의 8칸(클로드 활용 / 다른 AI / 기타 프로그램 / 내 생산성 루틴 / AI×신발 / AI×메디쏠라 / AI×골프 / AI×가족·민주). 도구·기능 관련 주장은 2025–2026 자료만 사용했고, 원문을 직접 확인하지 못한 항목은 **[미확인]**으로 표시했다. 조사 중 웹검색 예산이 소진되어 일부 항목(골프존, 네이버 스마트스토어 판매자용 AI, 한국어 LLM 비교 등)은 공식 페이지 직접 조회(fetch)만으로 보완했으며, 보완되지 않은 부분은 각 절의 Gaps에 명시했다.

---

## KQ1. AI 생산성 효과의 증거 — 지식노동·소상공인에게 무엇을 뜻하는가

### Takeaway
통제실험들은 "정형적이고 AI가 잘하는 과업(글쓰기·고객응대·아이디어·분석 초안)"에서 14~40% 수준의 시간 단축과 품질 향상을 일관되게 보여주지만, AI 역량 밖의 과업에서는 오히려 정답률이 떨어지고(과신), 숙련된 전문가의 실제 작업에서는 2025년 초 기준 19% *느려진* RCT도 있다. 비개발자 1인 사업자에게 가장 중요한 함의는 (1) 초안·반복 업무에 집중 투입하면 이득이 크고, (2) 검토 시간이 이득을 잠식할 수 있으며, (3) "내가 틀렸는지 알 수 없는 영역"에서 AI를 믿으면 손해라는 것이다.

### Cited Findings
- **콜센터 RCT(Brynjolfsson·Li·Raymond)**: 고객지원 상담원 5,179명, 생성형 AI 보조 도구 단계적 도입. 시간당 해결 건수 평균 **+14%**, 신입·저숙련 **+34%**, 숙련자는 효과 미미. 고객 감정 개선, 이직 감소. NBER WP 31161(2023.4, 2023.11 개정) → *Quarterly Journal of Economics* 140(2), 889–942 (2025) 게재 — [NBER](https://www.nber.org/papers/w31161)
- **전문직 글쓰기 RCT(Noy & Zhang)**: 대졸 전문직 444명(마케터·그랜트라이터·컨설턴트·데이터분석가·HR·매니저), 20~30분짜리 실제 업무형 글쓰기(보도자료·보고서·분석계획·민감한 이메일). ChatGPT 집단은 소요시간 **−10분(−37%; 대조군 27분)**, 평가자 점수 **+0.45 SD**. 저능력 작업자가 더 이득을 봐 불평등 감소. "ChatGPT는 주로 노력을 *대체*하고 기술을 보완하기보다, 작업을 초안작성→아이디어·편집으로 재구성". 직무만족·자기효능감 증가. 처치군의 81%가 실제 사용, 유용성 자평 4.4/5 — [MIT 워킹페이퍼 PDF(2023.3.2)](https://economics.mit.edu/sites/default/files/inline-files/Noy_Zhang_1.pdf). 최종본은 *Science* 381(6654), 2023.7 게재 — [DOI](https://www.science.org/doi/10.1126/science.adh2586) **[미확인: 원문 403으로 접근 불가. 게재본 수치(453명, 시간 −40%, 품질 +18%)는 기억 기반이므로 보고서에는 워킹페이퍼 수치를 사용 권장]**
- **"들쭉날쭉한 경계"(Dell'Acqua 외, BCG 컨설턴트 758명 RCT)**: 조건은 AI 없음 / GPT-4 / GPT-4+프롬프트 교육. *경계 안* 과업(제품 아이디어·시장진입·글쓰기·설득)에서는 **+12.2% 과업 완료, 약 25% 빠름, 품질 상승**(HBS 요약 페이지는 "약 32%"라고 기술 — 워킹페이퍼 초록의 "40% 이상"과 수치 차이 있음, 아래 Gaps). *경계 밖* 과업(스프레드시트+인터뷰 노트를 교차 검토해야 하는 브랜드 전략 케이스)에서는 정답률 **대조군 84.5% vs GPT-4 70.6% vs GPT-4+교육 60.0%**. 실패 원인은 과업 지식 부족이 아니라 "AI 분석을 믿고 잘못된 결론까지 따라간" **과신**. 하위 50% 성과자 **+31%**, 상위 50% **+11%** 개선(스킬 평준화). 2023.9 워킹페이퍼 → *Organization Science* 37(2): 403–423 (2026.3) 게재 — [HBS Digital Data Design Institute](https://aiinstitute.hbs.edu/?p=29980)
- **METR 2025 RCT(숙련 개발자, 2025.7.10 공개)**: 대형 오픈소스 저장소(평균 22k+ 스타, 100만+ 라인)에 수년간 기여한 개발자 16명, 실제 이슈 246개를 AI 허용/불허로 무작위 배정(주로 Cursor Pro + Claude 3.5/3.7 Sonnet, 시급 $150). 결과: AI 허용 시 **19% 더 오래 걸림**. 사전 예측은 "+24% 빨라질 것", 종료 후 체감도 "+20% 빨라졌다"였음(인식과 측정의 괴리 약 40%p). 저자 명시 한계: 표본 16명은 "0 가속 기각에 간신히 충분", AI가 크게 도움된다고 믿는 개발자가 참여를 꺼렸을 가능성, 50시간 이상 Cursor 학습효과 배제 불가, 2025년 초 도구 기준 스냅샷이며 다른 도메인·신입·낯선 코드베이스에는 일반화 불가 — [METR](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/)
- **METR 2026.2.24 설계 변경 공지**: 2025년 말 도구로 진행한 2차 연구에서 원래 개발자군 **−18%(=18% 가속, CI −38%~+9%)**, 신규 모집 개발자 **−4%(CI −15%~+9%)**로 둘 다 CI가 0을 포함. "AI 없이 일하기 싫어서" 참여 거부·과업 미제출(30~50%)·시급 $150→$50 인하 등 선택효과와 다중 에이전트 병행으로 시간 측정이 불안정해져 설계를 재편. 저자 결론: 2026년 초 개발자는 2025년 초보다 더 가속될 가능성이 높지만 "매우 약한 증거"이며 추정치는 하한에 가깝다 — [METR](https://metr.org/blog/2026-02-24-uplift-update/)
- **METR 2026.5.11 자기보고 설문**: 기술직 349명(SW 엔지니어 87, 연구자 71, 학계 129, 창업자·매니저 48; 2026.2–4 조사, 응답률 약 2%의 편의표본). 자기보고 "가치" 변화 중앙값 **1.4~2×**, "속도" 중앙값 **3×**. 저자 스스로 "설문 결과는 현실에 근거하지 않을 수 있다", 이전 RCT에서 자기보고가 약 40%p 과대였음을 경고. Claude Code/Codex 사용자·스타트업·고사용자가 더 높은 이득을 보고, METR 직원 자신은 가장 낮게 보고 — [METR](https://metr.org/blog/2026-05-11-ai-usage-survey/)
- **덴마크 행정자료(Humlum & Vestergaard, NBER WP 33777 "Still Waters, Rapid Currents")**: 노출 직종 11개, 근로자 2.5만 명·사업장 7천 개. ChatGPT 출시 2년 후 **소득·근로시간에 정밀한 0 효과**(2% 이상 효과 배제). 도입자는 AI 관련성이 높은 고임금 직종으로 이동하는 경향 — [NBER](https://www.nber.org/papers/w33777); 초기 버전 [BFI WP 2025-56](https://bfi.uchicago.edu/wp-content/uploads/2025/04/BFI_WP_2025-56-3.pdf)
- **비판적 사고 설문(Lee, Sarkar 외, Microsoft Research·CMU, CHI 2025)**: 지식노동자 319명, 실제 GenAI 사용 사례 936건. **AI에 대한 신뢰가 높을수록 비판적 사고↓, 자기 능력에 대한 자신감이 높을수록 비판적 사고↑.** 비판적 사고의 성격이 "정보 검증·응답 통합·과업 관리"로 이동. 고위험 과업에서는 AI를 쓸 때 오히려 검증 노력을 더 들이고, 시간압박 하의 저위험 루틴 과업에서는 덜 들임 — [논문 PDF](https://advait.org/files/lee_2025_ai_critical_thinking_survey.pdf), [Microsoft Research](https://www.microsoft.com/en-us/research/?p=1135061)
- **번아웃·"항상 켜짐" 증거(Upwork Research Institute, 2024.7.23)**: AI 사용 직원의 **77%**가 "AI가 업무량을 늘렸다"고 응답(경영진 96%는 생산성 향상 기대). 추가 업무의 내역: AI 산출물 검토 39%, 도구 학습 23%, AI 때문에 늘어난 일 21%. 정규직 71% 번아웃, 1/3은 6개월 내 이직 의향. 표본 2,500명(미·영·호·캐) — [Upwork 보도자료](https://www.upwork.com/press/releases/upwork-study-finds-employee-workloads-rising-despite-increased-c-suite-investment-in-artificial-intelligence)

### Inferences
- 사장님의 업무 중 "경계 안"에 해당하는 것: 제안서·견적서 초안, 가맹 상담 후속 메일, 블로그·인스타 문안, 회의록 정리, 상권 자료 요약. 여기서는 Noy&Zhang·Dell'Acqua 수준(시간 25~40% 단축)의 이득을 기대할 수 있다.
- "경계 밖"에 해당하는 것: 특정 입지의 임대차 조건·권리금 판단, 가맹본부 계약조항 해석, 세무·법무, 숫자가 섞인 복수 자료의 교차검증. Dell'Acqua의 60~70% 정답률 사례처럼 **AI를 믿을수록 틀릴 확률이 올라가는 영역**이므로, AI는 "질문 생성기·체크리스트"로만 쓰고 결론은 사람이 낸다.
- METR의 "체감 +20% / 실측 −19%" 괴리는 비개발자에게도 적용된다고 보는 것이 안전하다. 따라서 루틴에 **주 1회 실측(타이머)** 을 넣어 체감이 아닌 측정으로 AI 투입 범위를 조정해야 한다.
- Upwork의 "검토 39%"와 Lee 외의 "고위험일수록 검증 노력↑"은, 검증 비용을 줄이는 설계(템플릿·예시·출처 강제)가 생산성의 핵심 변수임을 시사한다.
- 덴마크 결과는 "도구가 있어도 업무 재편(어떤 일을 AI에 넘기고 남는 시간을 무엇에 쓸지)이 없으면 성과로 이어지지 않는다"는 뜻으로 읽을 수 있다. 1인 사업자는 재편 권한이 100% 자신에게 있으므로 조직보다 유리하다.

### Gaps
- Dell'Acqua 품질 상승 수치가 출처별로 다름(HBS 요약 "약 32%" vs 2023 워킹페이퍼 초록 "40% 이상"). Organization Science 게재본 원문 미확인.
- Noy & Zhang *Science* 게재본 원문 미확인(403).
- 2024–2026년에 **소상공인·자영업자**를 직접 대상으로 한 통제실험은 이번 조사에서 찾지 못했음(검색 예산 소진). 위 증거는 모두 대기업·전문직·개발자 대상.
- "항상 켜짐" 번아웃에 대한 2025–2026 신규 데이터는 확보하지 못함(Upwork 2024가 최신 확인분).

---

## KQ2. 클로드(Claude) 생태계 2026 — 기능 확인과 소상공인 활용 사례

### Takeaway
2026년 10월 기준 공식 문서로 확인된 구성요소는 **Projects(프로젝트 지식+커스텀 지시+프로젝트별 메모리), Skills(SKILL.md 폴더, Pro 이상), 커넥터(Gmail·Calendar·Drive — 메일 발송·캘린더 생성 가능, 기본은 실행 전 승인), Claude Code 클라우드 세션(Pro·Max·Team), Routines(예약·API·GitHub 트리거, 연구 프리뷰, 최소 1시간 간격)** 이다. 이미 Claude Code 클라우드+GitHub Pages를 쓰는 사용자는 "Projects=업무 지식창고 / Skills=견적서·제안서 템플릿 / Routines=아침 브리핑·주간 리뷰 자동화"로 확장하는 것이 자연스럽다.

### Cited Findings
- **Projects**: 모든 플랜에서 생성 가능(무료는 5개 제한). 프로젝트 지식(문서·텍스트·코드)을 업로드하면 해당 프로젝트의 모든 대화에서 컨텍스트로 사용. 유료 플랜은 지식이 컨텍스트 한도에 근접하면 RAG 모드로 자동 확장. 커스텀 지시(모든 대화에 적용). 대화 간 컨텍스트는 공유되지 않으며(프로젝트 지식에 넣어야 함), 메모리는 Free/Pro/Max 기본 활성, **프로젝트별로 분리된 메모리** 유지, "계정 메모리 사용" 끄기 가능. 공유는 Team/Enterprise만 — [Claude 지원센터](https://support.claude.com/en/articles/9519177-how-can-i-create-and-manage-projects)
- **Skills(Agent Skills)**: 2025.10.16 발표, 2025.12.18 업데이트(조직 단위 관리·파트너 스킬 디렉터리·agentskills.io 개방 표준). 지시·스크립트·리소스를 담은 폴더(SKILL.md)로, 필요한 최소 정보만 로드. Claude 앱에서는 자동 적용되며 내장 **skill-creator** 로 커스텀 스킬 제작 가능. Claude Code에서는 anthropics/skills 마켓플레이스 플러그인 또는 `~/.claude/skills`에 수동 설치. 앱 사용 요건 **Pro·Max·Team·Enterprise**. 예시: 수식 있는 엑셀·PPT·워드·채움형 PDF 생성, 브랜드 가이드라인 준수, 회계 대사·보고서 자동화(라쿠텐). 보안: 스킬은 코드를 실행하므로 신뢰할 수 있는 출처만 사용 — [Claude 블로그](https://claude.com/blog/skills)
- **Google Workspace 커넥터(Gmail·Calendar·Drive)**: 모든 Claude/Claude Desktop 사용자에게 제공(Team/Enterprise는 관리자 활성화 필요). **Gmail**: 자연어 검색·읽기, 초안 작성, **발송·답장·전달**, 메타데이터 접근, 라벨·스레드 관리, 초안 목록(첨부파일은 메타데이터만, 본문 불가). **Calendar**: 공유 캘린더 포함 조회, 일정 생성·수정·삭제, 참석자 간 빈 시간 찾기, 참석자·RSVP 관리, 반복 일정. **Drive**: Docs·Sheets·Slides·PDF·이미지·MS Office 읽기, 공유·이동·휴지통, 업로드, 폴더 생성, Claude 생성 파일 저장(코드 실행·파일 생성 활성화 시). **기본값: 발송·전달·공유·삭제 등 실행 전 명시적 승인**. Docs/Sheets/Slides를 채팅 옆 패널에서 편집하는 기능은 베타 — [Claude 지원센터](https://support.claude.com/en/articles/10166901)
- **Claude Code 클라우드 세션**: Pro·Max·Team(Enterprise는 프리미엄 시트) 제공. 브라우저(claude.ai/code)·모바일 앱 Code 탭·Desktop·터미널 `claude --cloud`에서 시작, 노트북을 닫아도 계속 실행, 폰에서 확인·지시 가능. 플랜 사용량에 합산(별도 VM 요금 없음). 세션 공유(Pro/Max는 Private/Public), 자동 PR 수정(Auto-fix), 서브에이전트 지원. 제한: 저장소·PR은 GitHub 필요, 비활성 시 VM 회수(대화는 복원, 백그라운드 작업은 복원 안 됨) — [Claude Code 문서](https://code.claude.com/docs/en/claude-code-on-the-web)
- **Routines(연구 프리뷰)**: "프롬프트 + 저장소 + 커넥터"를 저장해 Anthropic 클라우드에서 자동 실행. 트리거 3종: **Scheduled**(시간별·일별·평일·주별·1회성; 정각 예약 시 수 분 지연 가능해 9:07처럼 권장; **최소 간격 1시간**), **API**(라우틴별 엔드포인트+베어러 토큰, `text` 페이로드는 신뢰되지 않는 데이터로 래핑), **GitHub**(PR·릴리스 이벤트). **Pro·Max·Team·Enterprise** 제공. 생성: claude.ai/code/routines, Desktop, CLI `/schedule`(예: `/schedule daily PR review at 9am`, `/schedule tomorrow at 9am, summarize yesterday's merged PRs`). 실행은 승인 없이 자율 진행(연결된 모든 커넥터의 쓰기 포함 → **불필요한 커넥터는 제거 권장**). 라우틴은 개인 계정 소유, 구독 사용량 차감, 예약 실행 계정당 100회/시간. 녹색 상태 = 인프라 오류 없음일 뿐 과업 성공 아님(로그 확인 필요). 아티팩트를 자동 발행해 "페이지를 최신으로 유지"하는 용도 명시 — [Claude Code 문서](https://code.claude.com/docs/en/routines)
- **세션 내 예약(`/loop`)과 Desktop 로컬 예약 작업**: 세션 범위 작업은 대화가 끝나면 종료되고 반복 작업은 7일 후 만료; 지속 예약은 Routines·Desktop 예약 작업·GitHub Actions로 — [scheduled-tasks](https://code.claude.com/docs/en/scheduled-tasks), [desktop-scheduled-tasks](https://code.claude.com/docs/en/desktop-scheduled-tasks)
- **소비자 데이터 학습 정책(2025.8.28 공지)**: Free/Pro/Max(그 계정의 Claude Code 포함)는 **사용자가 설정을 켠 경우에만** 학습에 사용. 켜면 보존 5년(신규·재개 대화만), 끄면 30일. 삭제한 대화는 학습 미사용. Team/Enterprise·API·Gov·Education은 적용 제외 — [Anthropic](https://www.anthropic.com/news/updates-to-our-consumer-terms)

### Inferences
- **제안서·견적서**: Projects에 (a) 과거 제안서 3~5건, (b) 가맹본부별 조건표, (c) 단가표를 넣고, Skill로 "견적서 생성 → xlsx 출력" 템플릿을 만들면 Skills 공식 예시(수식 포함 엑셀 생성)와 정확히 일치하는 사용법이다.
- **고객 후속관리**: Gmail 커넥터로 "지난 2주 답장 없는 가맹 문의 스레드 찾고 후속 메일 초안 작성"이 가능하며, 기본 승인 절차가 있어 오발송 위험은 낮다. 다만 Routines에 Gmail을 연결하면 승인 없이 발송될 수 있으므로, 자동 라우틴에는 **읽기 전용 목적만** 연결하거나 "초안만 작성하고 발송하지 말 것"을 프롬프트에 명시해야 한다.
- **상권·점포 분석**: Claude Code 클라우드 세션에서 공공데이터(상가정보 CSV 등)를 저장소에 넣고 분석 스크립트를 돌린 뒤 GitHub Pages로 리포트를 게시하는 흐름은 이미 쓰는 환경과 연속적이다. 단, 지도·유동인구 수치의 정확성 검증은 "경계 밖" 과업이므로 결론 전 원자료 재확인이 필요.
- **네이버 블로그·인스타 콘텐츠**: Projects의 커스텀 지시에 톤·금지표현·브랜드 용어를 고정하면 일관성이 확보된다. AI 기본법상 *이용자*는 규율 대상이 아니므로 블로그 글에 AI 표시 의무는 없으나(KQ5), 플랫폼 정책·독자 신뢰 차원에서 사실관계 검증은 필수.
- 고객 개인정보(이름·연락처·계좌)가 담긴 자료를 Projects에 올리는 것은 개인정보위 가이드(KQ5)와 충돌한다. 업로드 전 가명처리(이름→고객A)를 루틴화하고, Pro/Max 계정의 "모델 개선에 데이터 사용" 설정은 **끄는 것**이 안전하다.

### Gaps
- Claude.ai의 Notion·Slack 커넥터 공식 문서는 직접 확인하지 못함(검색 결과는 제3자 블로그뿐). 기능 범위는 **[미확인]**.
- 커넥터·Routines의 **한국어 서비스(네이버·카카오)** 연동은 공식 목록에 없음(확인된 범위에서는 GitHub·Slack·Linear·Google Drive 등). 네이버/카카오와의 연결은 API 또는 Zapier/Make 같은 중간 도구가 필요하다는 추정 — **[미확인]**.
- Claude Desktop의 Cowork·브라우저 기능 등은 이번 조사 범위에서 확인하지 않음.

---

## KQ3. 그 밖의 AI 도구(한국, 2026) — 무엇이 남고 무엇이 사라졌나

### Takeaway
네이버는 소비자용 챗봇 **CLOVA X를 2026.4.9 종료**하고 HyperCLOVA X를 산업용으로 돌렸으며, 회의록 분야는 클로바노트·티로·다글로가 경쟁 중이다. 카카오는 2025.9.25 톡채널용 AI 상담 **'카나나 상담매니저'** 를 정식 출시했다. 구글의 NotebookLM은 **'Gemini Notebook'** 이라는 이름으로 운영되며 한국어 출력을 지원하고 무료 플랜도 노트북 100개·소스 50개로 넉넉하다. ChatGPT·Gemini·Perplexity·이미지/영상 도구의 2026 한국어 성능 비교 자료는 이번 조사에서 확보하지 못했다.

### Cited Findings
- **네이버 CLOVA X 종료**: 2026.2.24 공지, **2026.4.9 서비스 종료**. 사유는 "더 넓은 산업군에서 HyperCLOVA X의 가치를 만들어나가는 실험"으로, 개인용 챗봇에서 산업 적용으로 방향 전환. 종료 후 데이터 복구 불가. 댓글에서 2025.11 트리플 스킬 종료, 2026.1 스킬 서비스 종료도 언급 — [GeekNews](https://news.hada.io/topic?id=26978)
- **HyperCLOVA X THINK**(2025.6.30): 단계적 추론·자기오류 점검·도구 선택을 하는 추론 모델, KoBALT-700·HAERAE-Bench 등 한국어 벤치마크 상위 주장, 오픈소스 계획. 판매자용 기능 언급 없음 — [네이버 보도자료](https://www.navercorp.com/media/pressReleasesDetail?seq=33066)
- **클로바노트**: 2020년 'AI 음성기록'으로 출발, 하이퍼클로바 기반 회의록 요약·화자분리 추가. 개인 무료 한도 월 300분(개인정보 활용 동의 시 600분), AI 요약 월 15회라는 2026.7 블로그 기술이 있으나 — [wikidocs 블로그](https://wikidocs.net/blog/@openwiki/23917/) **[미확인: 원문 403, 검색 스니펫 기준. 공식 요금 페이지 재확인 필요]**
- **티로(Tiro)**: 실시간 회의 전사·요약, 15개+ 언어(한국어·영어·일본어 명시), 데스크톱 앱은 봇 없이 시스템 오디오 녹음. 무료 체험 3주·최대 300분(노트당 50분). Lite 300분/월, **Pro 1,000분/월부터 화자분리** 제공, Max 무제한. 금액 미표시. 정확도는 "숫자·이름 완벽 정확" 등 벤더 주장만 — [tiro.ooo](https://tiro.ooo/)
- **다글로(Daglo)**: 회의·강의·영상·파일 전사, 화자분리(무료 1명·Pro 5명·Premium 50명), AI 요약·액션아이템, 유튜브 요약, 문서 번역. **무료 $0(1,000크레딧/월), Pro $11.66/월, Premium $16.66/월, Team 20,750원/시트/월**. 연 13M+ 시간 전사, ISO/IEC 27001 — [daglo.ai](https://daglo.ai/)
- **카나나 상담매니저(카카오)**: **2025.9.25 정식 출시**, 모든 톡채널 사업자 대상. 채널에 올린 매장정보·메뉴·소식 기반 자동응답, 질문 의도 파악, 1:1 채팅 주문·예약 자동 접수, 운영시간 설정(채팅 가능 시간 내/외/24시간), 문의 통계. 2024.10부터 베타, 주문·예약 업종 만족도 높음(수치 없음). 요금 미기재 — [카카오](https://www.kakaocorp.com/page/detail/11719)
- **카카오 톡채널 챗봇 요금 무료화**: 기존 월 5만 건 무료·초과 건당 3~40원이던 '일반 요금' 상품 전면 무료화 보도 — [데일리안](https://www.dailian.co.kr/news/view/1138780/), [카카오 공지](https://www.kakaocorp.com/page/detail/9756) **[시행 시점 미확인]**
- **Gemini Notebook(구 NotebookLM)**: 업로드한 소스 기반 답변+인용, 소스당 50만 단어 또는 200MB, 페이지 제한 없음(복제방지 PDF 불가). 플랜별 한도(변경 가능): **Standard(무료) 노트북 100개·소스 50개/노트북**, Plus 200/100, Pro 500/300, Ultra 500/500~600. 출력 언어 80개+ 중 **한국어 포함**(설정→Output Language; Audio Overview의 한국어 지원은 별도 확인 필요) — [플랜](https://support.google.com/gemininotebook/answer/16213268?hl=en), [언어](https://support.google.com/gemininotebook/answer/16261963?hl=en), [FAQ](https://support.google.com/gemininotebook/answer/16269187?hl=en)
- **인테리어 시각화(ReimagineHome.ai)**: 사진 한 장으로 인테리어 리디자인·버추얼 스테이징·정리, **상업공간(리테일 매장 레이아웃) 지원**, 50장 일괄 처리, 실제 구매 가능한 가구 소싱(미국 리테일러 중심). 무료 5개 디자인(유료와 동일 품질), Pro 무제한(가격 별도 페이지) — [reimaginehome.ai](https://www.reimaginehome.ai/)
- **제품 사진(Photoroom)**: 배경 제거(유료 플랜 핵심 도구, 크레딧 無), AI 배경, AI 그림자, 제품 스테이징, 일괄 처리. Pro 8,000크레딧·1,000내보내기/월, Max 25,000·3,000(비디오 생성 포함), Ultra 75,000·10,000(4K). 가격은 연간 결제 기준으로만 표시(USD 미표기), 무료 체험 있음 — [photoroom.com/pricing](https://www.photoroom.com/pricing)

### Inferences
- 회의·현장 상담 녹취는 **한국어 화자분리**가 핵심이므로 클로바노트(무료 한도 내) → 부족하면 다글로 Pro($11.66, 5명 화자) 순으로 올리는 것이 비용 효율적. 티로는 화자분리가 Pro(1,000분)부터라 1인 사업자에겐 과하다.
- 가맹 상담 전 녹음 고지는 필수(KQ5의 개인정보 원칙과 연결). 녹취 파일은 요약 후 원본 삭제 주기를 정해 둔다.
- 네이버 CLOVA X 종료는 "국내 소비자용 범용 챗봇에 업무를 묶지 말 것"의 신호다. 범용 사고·작성은 Claude/ChatGPT/Gemini, 한국어 음성·회의록·검색/쇼핑은 네이버·카카오 생태계 도구로 역할을 나누는 편이 안전하다.
- Gemini Notebook은 "가맹본부 정보공개서·계약서 모음"처럼 **출처가 고정된 문서 더미에 질문**하는 용도로 Claude Projects와 보완적이다(인용 표시가 강점).

### Gaps
- ChatGPT·Gemini·Perplexity·Claude의 **2026 한국어 성능 비교** 자료 미확보(검색 예산 소진). 카카오 '카나나' 앱·카카오톡 내 ChatGPT 제휴의 현황도 **[미확인]**.
- Midjourney·Flux·Canva AI 등 이미지 생성 도구의 2026 요금·상업 이용 조건은 확인하지 못함.
- 클로바노트 공식 요금·한도 미확인. 골프존 등 국내 골프 AI는 KQ7 참조.
- 네이버 스마트플레이스·스마트스토어 **판매자용 AI 기능**(상품명·상세페이지 자동생성 등)의 공식 사양은 확보하지 못함(KQ6 참조).

---

## KQ4. 자동화/"기타 프로그램" — 1인 사업자가 먼저 깔아야 할 것

### Takeaway
요금과 구조가 확인된 범용 자동화 도구는 Zapier(무료 100태스크/월, Pro 연간 $19.99/월~), Make(무료 1,000크레딧/월), n8n(Starter €20/월·2.5K 실행, 셀프호스팅 커뮤니티판 무료)이다. 다만 사장님의 핵심 채널이 카카오톡·네이버·Gmail이라면 **①카나나 상담매니저(톡채널 자동응답) → ②Claude의 Gmail·Calendar 커넥터 → ③Claude Code Routines(아침 브리핑·주간 리포트)** 순으로 "이미 가진 것"부터 켜는 것이 비용·학습 부담이 가장 적다. Zapier/Make/n8n은 네이버·카카오·스마트스토어처럼 Claude가 직접 못 닿는 곳을 잇는 데 한정해 투입한다.

### Cited Findings
- **Zapier**(2026.10.16 기준 페이지): Free $0·100태스크/월, Professional 연간 $19.99/월(월납 $29.99)·750태스크~, Team 연간 $69/월~. Copilot(베타) 무료는 일일 한도, AI by Zapier는 Pro 이상, Zapier Agents 기본 제공(Free 400 활동/월, Pro 1,500) — [zapier.com/pricing](https://zapier.com/pricing)
- **Make**: Free 플랜 **1,000크레딧/월**, 액션당 1크레딧 기본(AI Provider 사용 기능은 더 소모). Core/Pro 가격·한도는 페이지에서 미확인, Maia AI 어시스턴트·AI 에이전트·MCP 서버 메뉴 존재 — [make.com/en/pricing](https://www.make.com/en/pricing)
- **n8n**: Starter **€20/월(연납)** 2.5K 워크플로 실행·동시 5·로그 7일, Pro €50/월 10K 실행·로그 30일. 셀프호스팅 커뮤니티판 GitHub 제공. AI Agent 노드·MCP 서버 트리거/클라이언트·툴 호출 사람 승인 기능, Starter에 API 키 없이 쓰는 AI 모델 포함 — [n8n.io/pricing](https://n8n.io/pricing)
- **카카오 톡채널 자동응답**: 카나나 상담매니저(2025.9.25)로 매장정보 기반 자동응답·주문·예약 접수·운영시간 설정 가능 — [카카오](https://www.kakaocorp.com/page/detail/11719)
- **Claude Routines**: 예약(최소 1시간 간격)·API·GitHub 트리거, 커넥터 쓰기 포함 자율 실행, 아티팩트 자동 갱신 가능 — [Claude Code 문서](https://code.claude.com/docs/en/routines)
- **Claude Google Workspace 커넥터**: Gmail 발송·Calendar 생성·Drive 저장까지 가능, 실행 전 승인 기본 — [Claude 지원센터](https://support.claude.com/en/articles/10166901)

### Inferences
- **먼저 설정할 3가지(비용 0~약 3만원/월)**: (1) 톡채널 카나나 상담매니저에 가맹 FAQ·상담 가능 시간·자료 요청 양식 등록, (2) Claude Projects 3개(가맹영업 / 점포개발·인테리어 / 신발·메디쏠라) + Gmail·Calendar 커넥터, (3) Routines 2개(평일 아침 브리핑, 금요일 주간 리뷰; 둘 다 "초안·요약만, 발송 금지"로 프롬프트).
- 그 다음 단계(필요할 때만): 스마트스토어·쿠팡 주문 알림 → 구글시트 집계는 Zapier Free(100태스크)로 시작해 월 100건 넘으면 Make Free(1,000크레딧)로 이동. n8n은 셀프호스팅이 가능하지만 서버 관리 부담이 있어 1인 사업자에겐 후순위.
- Notion·구글시트는 "AI가 읽고 쓸 수 있는 단일 장부" 역할이 핵심이다. Claude의 Drive 커넥터가 Sheets를 읽으므로, 고객·점포 파이프라인은 Google Sheets 한 장으로 유지하는 것이 자동화 연결점이 가장 많다(Notion 커넥터는 공식 범위 미확인).

### Gaps
- 네이버 스마트플레이스·스마트스토어의 공식 API/자동화 가능 범위, 카카오 톡채널의 2026 요금 체계는 **[미확인]**.
- Google Workspace 자체 AI(Gemini for Workspace) 요금·기능은 조사하지 않음.
- Notion AI 2026 요금·기능 미확인.

---

## KQ5. AI와 함께하는 생산성 루틴 설계 + 가드레일(개인정보보호법·AI 기본법)

### Takeaway
루틴 설계의 근거는 KQ1의 세 가지 사실 — (a) 초안·요약류는 크게 빨라지고, (b) 검토 비용이 이득을 잠식하며, (c) 체감은 실측보다 낙관적이다 — 에서 나온다. 따라서 "아침 브리핑(읽기만) → 업무 중 초안 위임 → 저녁 로그(사실 기록) → 주간 리뷰(실측·정리)"의 4단 구조에, 사실확인 규칙과 개인정보 처리 규칙을 붙인다. 법적으로는 **AI 기본법(2026.1.22 시행, 과태료·사실조사 1년 이상 유예)** 은 AI *사업자*를 규율하며 단순 *이용자*는 제외되고, **개인정보위 이용자 가이드(2026.5.19)** 는 "주민번호·계좌 등 입력 금지, 학습 옵트아웃, 국외이전 확인, 업무 정보도 자유롭게 넣지 말 것"을 권고한다.

### Cited Findings
- **AI 기본법 시행**: 「인공지능 발전과 신뢰 기반 조성 등에 관한 기본법」 및 시행령 **2026.1.22 시행**. 규율 대상은 *인공지능사업자*(개발사업자·이용사업자)이며 **"인공지능제품·서비스를 제공받는 자(이용자)는 규율 대상에서 제외"**. 투명성 의무(법 31조, 영 23조): 고영향·생성형 AI 사업자는 *사전 고지*(계약서·약관·화면 등)와 *표시*(일반 생성물은 사람이 인식 가능한 표시 또는 워터마크 등 기계판독 방식, 딥페이크는 명확한 표시만). **예외: 활용 사실이 명백한 경우, 사업자 내부 업무 용도로만 사용하는 경우.** 제재: 표시 위반 시정명령, 사전고지 위반 **3천만원 이하 과태료**. 고영향 AI(채용·대출심사 등)는 위험관리·설명·이용자보호·사람의 관리감독·문서 5년 보관. 과기정통부는 **사실조사·과태료 처분에 최소 1년 이상 유예(계도기간)**, 사실조사는 인명사고·인권훼손 같은 극히 예외적 경우에만 — [법무법인 세종 뉴스레터 2026.2.11](https://www.shinkim.com/kor/media/newsletter/pdf/3114), [영문판](https://www.shinkim.com/eng/media/newsletter/3117), [과기정통부 보도참고 2026.1.28](https://www.korea.kr/briefing/pressReleaseView.do?newsId=156741740), [인공지능기본법 지원데스크(080-850-2546, 생성형 AI 투명성 확보 가이드라인 등 제공)](https://www.sw.or.kr/AI_act_helpdesk/main.jsp), 요약 [Carat](https://carat.im/blog/ai-basic-law-summary)
- **개인정보위 '생성형 AI 서비스 이용자를 위한 개인정보 보호 가이드'(2026.5.19 발간)**: 주민번호·여권번호·계좌번호 등 입력 금지, 여러 정보 결합으로 식별 가능한 내용 주의; 서비스별 **학습 활용 옵트아웃** 설정; 대화기록 저장 기본값 점검, '삭제'가 즉시 삭제가 아닐 수 있음; 서버가 해외면 **국외이전**(국가·항목·목적·보유기간·이전받는 자) 확인; 답변에 개인정보가 나오면 캡처 후 삭제 요청; 외부 연동(일정·회의록)은 필요한 권한만; **업무 정보는 개인정보가 아니어도 자유롭게 입력하지 말 것(미공개 정보·내부 의사결정·계약 정보)**, 고객·거래처 개인정보 입력 시 외부 전달 위험, 조직은 학습 미사용이 계약으로 보장되는 기업용 라이선스 사용 — [아주경제 권기원 칼럼 2026.6.25(가이드 원문 아님)](https://www.ajunews.com/view/20260625083559981)
- **Anthropic 소비자 데이터 정책**: Free/Pro/Max는 설정을 켠 경우에만 학습, 켜면 5년·끄면 30일 보존, Team/Enterprise/API 제외 — [Anthropic](https://www.anthropic.com/news/updates-to-our-consumer-terms)
- **검증 노력의 분포**: 고위험 과업에서는 AI 사용 시 검증 노력이 커지고, 시간압박 하의 저위험 루틴 과업에서는 줄어듦; AI 신뢰↑→비판적 사고↓ — [Lee 외 CHI 2025](https://advait.org/files/lee_2025_ai_critical_thinking_survey.pdf)
- **검토가 늘리는 업무량**: AI 사용자의 추가 시간 중 검토 39%·학습 23% — [Upwork](https://www.upwork.com/press/releases/upwork-study-finds-employee-workloads-rising-despite-increased-c-suite-investment-in-artificial-intelligence)
- **체감 vs 실측 괴리**: 체감 +20% vs 실측 −19% — [METR](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/)
- **Routines의 예약 특성**: 최소 1시간 간격, 정각보다 9:07처럼 분 단위 지정 권장, 커넥터 쓰기 자율 실행 — [Claude Code 문서](https://code.claude.com/docs/en/routines)
- **Projects 메모리 분리**: 프로젝트별 메모리, 계정 메모리 분리 옵션 — [Claude 지원센터](https://support.claude.com/en/articles/9519177-how-can-i-create-and-manage-projects)

### Inferences
- **법 적용 판단(추론)**: 사장님이 Claude로 제안서·블로그를 쓰는 것은 '이용자'로서 AI 기본법 규율 밖. 반면 톡채널 AI 상담봇을 고객에게 *제공*하면 '이용사업자'에 해당할 수 있어 "AI 상담입니다" 사전 고지를 채널 소개·첫 메시지에 넣는 것이 안전(카카오 플랫폼이 표시하더라도 자체 고지 권장). 고영향 AI(채용·대출심사)는 해당 없음. 계도기간 1년+이므로 2027년 초까지 정비하면 됨.
- **개인정보 처리 루틴(추론)**: ① 고객 자료는 가명화 후 입력(이름→고객A, 전화→끝 4자리 삭제), ② Pro/Max의 학습 설정 OFF, ③ 녹취는 사전 고지 + 요약 후 30일 내 원본 삭제, ④ 계약서 원문 대신 조항 발췌만 업로드, ⑤ 커넥터는 필요한 계정만(가족 캘린더와 업무 캘린더 분리).
- **사실확인 규칙(추론)**: Dell'Acqua의 과신 메커니즘을 막으려면 "숫자·날짜·법조문·고유명사"는 AI 출력에 출처 링크를 요구하고, 출처 없는 숫자는 문서에 넣지 않는다. 블로그·제안서에 쓰는 통계는 원문 1회 열람을 규칙화.
- **번아웃 방지(추론)**: Routines가 밤새 돌더라도 *읽는 시간*은 아침 1회로 고정하고, 야간 알림은 끈다. "AI가 더 할 수 있다"는 이유로 업무 범위를 넓히면 Upwork의 77%가 된다 — 주간 리뷰에서 "AI로 줄인 시간을 어디에 썼는가"를 기록해 확장 압력을 가시화.
- **개인 지식창고(추론)**: 업무 지식은 Claude Projects(대화형)+Gemini Notebook(출처 고정 문서)+Google Sheets(정형 데이터)의 3층으로, 각 층의 "진실의 원천"을 하나로 정한다. 저녁 로그는 GitHub Pages 저장소의 마크다운 일기로 쌓으면 Claude Code 세션이 그대로 읽을 수 있다.

### Gaps
- 개인정보위 가이드 **원문**(pipc.go.kr)은 확인하지 못했고 칼럼 요약에 의존. 소상공인용 '개인정보보호법 준수 체크리스트'(개인정보위 발간물) 최신판 미확인.
- 과기정통부의 '생성형 AI 투명성 확보 가이드라인' 본문(텍스트 생성물의 표시 방식 세부)은 미확인. Carat 요약은 "텍스트는 비가시성 표시 기준에서 제외"라 기술하나 1차 자료로 검증 못 함 **[미확인]**.
- 번아웃·수면·"항상 켜짐"에 대한 2025–2026 학술 증거는 미확보.

---

## KQ6. AI × 신발 사업·메디쏠라 — 수요예측·상품사진·리스팅·CS

### Takeaway
확인된 것은 (1) 제품 사진 자동화 도구(Photoroom: 배경제거·AI 배경·그림자·일괄처리), (2) 톡채널 CS 자동화(카나나 상담매니저: 주문·예약 접수), (3) 쿠팡이 소상공인 판매자에게 AI 기반 판매데이터 분석·맞춤 마케팅·스마트 광고를 제공한다는 2025.10 보도, (4) Claude Skills로 엑셀 수식·보고서 생성이 가능하다는 점이다. 소규모 신발 셀러용 **수요예측 도구의 효과 증거와 네이버 스마트스토어 판매자용 AI 사양은 확보하지 못했다** — 이 단계에서는 "구글시트 판매 데이터 + Claude 분석"으로 시작하는 것이 근거 있는 선택이다.

### Cited Findings
- **Photoroom**: 배경 제거는 유료 플랜 핵심 도구(크레딧 미소모), AI 배경(Pro 4,000 기본 생성), AI 그림자(Pro 800), 제품 스테이징, 일괄 처리(내보내기 한도 차감: Pro 1,000/월, Max 3,000, Ultra 10,000) — [photoroom.com/pricing](https://www.photoroom.com/pricing)
- **쿠팡 판매자 AI(2025.10.31 보도, 2025 대한민국 소상공인 대회)**: 전체 판매자 중 약 75%가 중소상공인. AI 기반 고객행동 분석, 반품 피드백 시스템, 스마트 광고 솔루션, AI 상품 추천·물류 최적화·판매 데이터 분석·맞춤형 마케팅 지원 — [경기신문](https://www.kgnews.co.kr/news/article.html?no=871738)
- **네이버플러스 스토어(2024.11.28 발표)**: AI 쇼핑 앱, 검색 의도를 추론해 설명하는 'AI 쇼핑 추천' 베타 예정, 네이버배송(지금·새벽·희망일). 업계는 광고비 상승·가격비교 노출 축소로 소상공인 부담을 우려 — [청년일보](https://www.youthdaily.co.kr/news/article.html?no=172131) (2026 판매자용 기능 자료는 아님)
- **카나나 상담매니저**: 1:1 채팅 주문·예약 자동 접수, 매장정보 기반 답변 — [카카오](https://www.kakaocorp.com/page/detail/11719)
- **Claude Skills 예시**: 수식 포함 엑셀, 회계 대사·보고서 자동화 — [Claude 블로그](https://claude.com/blog/skills)
- **경계 안/밖 원칙**: 숫자 교차검증 과업에서 AI 과신 시 정답률 하락 — [HBS](https://aiinstitute.hbs.edu/?p=29980)
- **Gemini Notebook**: 소스 고정 문서에 인용 기반 질의, 한국어 출력 — [플랜](https://support.google.com/gemininotebook/answer/16213268?hl=en)

### Inferences
- **재고·수요(추론)**: 소량 SKU 신발 사업은 전용 수요예측 SaaS보다 "주간 판매·사이즈별 재고·입고 리드타임"을 구글시트 한 장에 기록하고, 월 1회 Claude(Projects+Drive 커넥터)에 "사이즈별 품절 위험·과잉 재고·재주문 시점" 분석을 시키는 편이 비용 대비 합리적. 단, 예측 숫자는 "경계 밖"에 가까우므로 *발주 결정 전 과거 3개월 실적과 대조*를 규칙화.
- **상품 사진(추론)**: 신발은 색·소재 재현이 핵심이라 AI *생성* 이미지보다 실촬영+Photoroom(배경·그림자·일괄 처리)이 반품 리스크가 낮다. 라이프스타일 컷은 AI 스테이징으로 시도하되, 실제 제품과 다른 디테일(스티치·로고)이 생기는지 검수.
- **리스팅(추론)**: 상품명·상세페이지 문안은 Claude Projects에 "스마트스토어 금칙어·브랜드 톤·사이즈 가이드"를 넣고 생성 → 사람이 소재·치수·원산지 같은 사실 항목만 재확인. 리뷰 답글도 동일 프로젝트에서 처리.
- **메디쏠라(브랜드)**: 브랜드 자료(기획서·성분/소재표·고객 FAQ)를 Gemini Notebook 한 권에 고정해 "근거 있는 문안"만 쓰게 하고, 상담은 톡채널 카나나로 1차 응대. 효능·의료적 표현은 AI가 만들어도 광고법 검토 대상이므로 사람이 최종 확인(추론; 관련 법령 미조사).

### Gaps
- 소규모 의류·신발 셀러용 AI 수요예측 도구의 효과 증거·요금(2025–2026) 미확보.
- 네이버 스마트스토어 판매자센터의 AI 상품등록·상세페이지·광고(클로바 for AD 등) 공식 사양 **[미확인]**.
- 쿠팡 윙(Wing)의 2026 AI 판매자 도구 세부 미확인.
- 메디쏠라의 제품군(식품/화장품/의료기기 여부)을 알 수 없어 표시·광고 규제는 다루지 못함.

---

## KQ7. AI × 골프 — 아마추어에게 효과 있는 것

### Takeaway
2026년 기준 확인된 선택지는 **Sportsbox AI 3D Golf(무료 월 5스윙, 유료 $9.16/월)**, **HackMotion 손목 센서($275~$915, '신규 사용자 89% 개선' 벤더 주장)**, **V1 Golf(영상 분석·코치 연결)**, **Arccos(센서 $249.99, '첫해 핸디캡 25% 감소' 벤더 주장)** 이며, 독립적 효과 연구는 찾지 못했다. 근거 수준상 가장 설득력 있는 접근은 "라운드 데이터(Arccos류)로 약점을 숫자로 찾고 → 그 약점만 영상/센서로 교정 → 사람 코치에게 월 1회 검수"다.

### Cited Findings
- **Sportsbox AI**: 3D 모션 분석 기반 코칭 앱, 3D 데이터에 대해 질문하는 AI 전문가 'SAMI', 자동 연습·스윙 비교. 소비자 요금 **Free(월 5스윙, 목표 1개, 3D 플레이어) / $9.16/월(무제한 스윙·목표, 2D·3D 비교, AI Expert)**. 코치 500+·골퍼 5만+. 2026.10.6 TaylorMade와 마커리스 3D 드라이버 피팅 제휴. **개선 효과 수치 없음** — [sportsbox.ai](https://www.sportsbox.ai/)
- **HackMotion**: 손목 각도 실시간 측정 센서, Core $275~ / Plus $420~(퍼팅 포함) / Pro $915~. 앱: 스윙 결함 표시, 실시간 코칭, 진동 피드백 드릴, 진행 추적. 벤더 주장 "신규 사용자 89%가 개선"(정의·측정법 미제시), 독립 연구 없음 — [hackmotion.com](https://hackmotion.com/)
- **V1 Golf**: 영상 분석·진행 추적·자가 훈련, 앱 내 코치 연결(세컨드 오피니언). 요금은 사이트에 미표시 — [v1sports.com](https://v1sports.com/); 제3자(벤더 GOATY 운영 RotarySwing) 비교표는 V1 $9.99~$19.99/월, Sportsbox $19.99~$39.99/월, GOATY $25/월로 기재 — [rotaryswing.com](https://rotaryswing.com/best-ai-golf-swing-analyzer-2026) **[벤더 자료, 수치 불일치 주의: Sportsbox 공식은 $9.16/월]**
- **Arccos**: 자동 샷 추적(클럽·라운드), Strokes Gained 분석, AI Strategy(15억 샷 기반 클럽·타깃 추천), Plays-Like 거리. 센서 **$249.99**, 연회비 미표시. "회원 평균 첫해 핸디캡 **25%** 감소"(측정 방법·표본 미제시) — [arccosgolf.com](https://www.arccosgolf.com/)
- **AI 과신 일반 원칙**: AI 신뢰↑→비판적 사고↓ — [Lee 외 CHI 2025](https://advait.org/files/lee_2025_ai_critical_thinking_survey.pdf)

### Inferences
- 아마추어의 흔한 실패는 "스윙 데이터는 많은데 무엇을 고칠지 모름"이다. Strokes Gained는 *어디서 타수를 잃는지*(퍼팅/어프로치/티샷)를 알려주므로 교정 대상 선정의 1순위 데이터. 이후 영상(Sportsbox 무료 5스윙/월로 시작) 또는 손목 센서(HackMotion은 손목 결함이 확인된 경우에만)로 단일 과제를 교정.
- Claude 활용: Arccos 라운드 요약·스윙 메모를 Projects에 쌓고 "지난 4주 데이터로 연습 계획 1개만 제안"을 받으면 과잉 교정을 막는다. 단, AI의 스윙 조언은 영상·데이터 없이 텍스트만으로는 신뢰도가 낮으므로 **사람 코치의 월 1회 검수**를 전제.
- 비용: 무료(Sportsbox Free+스코어 앱) → $9.16/월 → 센서($250~)의 3단계로, 3개월 데이터가 쌓인 뒤에만 다음 단계로 올린다.

### Gaps
- **골프존 AI(GDR·스윙 분석)**의 2026 기능·요금 자료 미확보(검색 예산 소진, 공식 페이지 미조회).
- 아마추어 대상 AI 스윙 앱 효과에 관한 **독립 연구/학술 증거 없음**(모두 벤더 주장).
- Arccos 연회비, V1 Golf 정확한 요금 미확인.

---

## KQ8. AI × 가족·민주 — 가정 운영, 임신·육아 정보, 관계 조언의 한계

### Takeaway
가정 운영(공유 캘린더·식단·여행)은 Claude의 Google Calendar 커넥터(공유 캘린더 조회·일정 생성·빈 시간 찾기)로 바로 가능하고, 육아 자료는 Gemini Notebook처럼 **출처 고정형** 도구가 맞다. 임신·건강 정보는 2026년 연구에서도 모델 간 정답률 편차(61~78%)와 "모든 모델에서 유해 응답 발생"이 확인되므로 *질문 정리용*으로만 쓰고 결정은 의료진과 한다. 관계·감정 문제는 Stanford 연구가 "치료사 대체 금지, 저위험 용도(일기·성찰·코칭)만"을 권고한다.

### Cited Findings
- **Claude Google Calendar 커넥터**: 공유 캘린더 포함 조회, 일정 생성·수정·삭제, 참석자 간 빈 시간 찾기, 반복 일정; 실행 전 승인 기본 — [Claude 지원센터](https://support.claude.com/en/articles/10166901)
- **Gemini Notebook**: 업로드 자료 기반 인용 답변, 무료 플랜 노트북 100개·소스 50개, 한국어 출력 — [플랜](https://support.google.com/gemininotebook/answer/16213268?hl=en), [언어](https://support.google.com/gemininotebook/answer/16261963?hl=en)
- **의료 정보 정확도(2026)**: 태아 중추신경계 MRI 텍스트 기반 진단 추론에서 주진단 일치율 DeepSeek 77.6%, Gemini 69.4%, ChatGPT 61.2%(단일기관·후향·텍스트만). 저자: "자율적 임상 진단·상담을 지지하지 않음, 감독 하 의사결정 지원만" — *Medicine* 2026; 채식 영양 질문에서는 **모든 모델에서 잠재적 유해 응답 발생**, 특히 "취약한 생애 단계(임신 등)·만성질환·증상 분류"에서 주의 — *Frontiers in Public Health* 2026; 간질성 방광염 질문에서 안전하지 않은 응답 5.2%(ChatGPT)~8.6%, "임상의 평가를 대체할 수 없음" — *Frontiers in Public Health* 2026. 출처: [Europe PMC 검색 결과](https://www.ebi.ac.uk/europepmc/webservices/rest/search?query=%28ChatGPT%20OR%20%22large%20language%20model%22%29%20AND%20%28pregnancy%20OR%20perinatal%20OR%20obstetric%29%20AND%20accuracy%20AND%20PUB_YEAR%3A%5B2024%20TO%202026%5D&format=json&resultType=core&pageSize=6)
- **산과 환자 교육 연구(2025)**: 무통분만(labor epidural) 질문에 대한 ChatGPT 등 챗봇의 정확도·감정 톤·가독성 연구 다수(*Int J Obstet Anesth* 2025 3편), 주산기 정보 정확도 연구(*PEC Innovation* 2025), 임신부 구강건강 질문 연구(*BMC Oral Health* 2025). 스니펫에 정확도 %는 없음 — [PubMed 검색](https://pubmed.ncbi.nlm.nih.gov/?term=ChatGPT+pregnancy+questions+accuracy) **[초록 미확인]**
- **치료용 챗봇 위험(Stanford HAI, 2025)**: 인기 치료 챗봇 5종(Pi, 7cups Noni, Character.ai Therapist 등) 실험. 알코올의존·조현병에 우울증보다 큰 낙인, 자살사고·망상 상황에서 도전 대신 조장(실직 후 "25m 넘는 다리" 질문에 다리 높이 안내), 신형·대형 모델도 개선 없음. 권고: **현재 LLM은 인간 치료사 대체 불가**, 보험·행정 보조나 "일기·성찰·코칭" 같은 저위험 용도가 적합 — [Stanford HAI](https://hai.stanford.edu/news/exploring-the-dangers-of-ai-in-mental-health-care)
- **AI 신뢰와 비판적 사고의 역관계** — [Lee 외 CHI 2025](https://advait.org/files/lee_2025_ai_critical_thinking_survey.pdf)
- **개인정보 가이드**: 외부 연동은 필요한 권한만, 가족 등 제3자 정보 입력 주의 — [아주경제 칼럼](https://www.ajunews.com/view/20260625083559981)

### Inferences
- **가정 운영(추론)**: 가족 공유 캘린더를 업무 계정과 분리해 커넥터에 연결하고, 일요일 저녁 "다음 주 가족 일정 충돌·빈 저녁 2개 찾기"를 Claude에 맡긴다. 식단은 "냉장고 재료+알레르기+예산"을 Projects 지시에 고정해 주간 식단·장보기 목록을 생성(영양 수치는 참고치로만).
- **여행 계획(추론)**: 일정 초안·동선·체크리스트는 경계 안 과업이라 효율이 높다. 다만 영업시간·요금·예약 가능 여부는 환각이 잦은 항목이므로 공식 사이트 1회 확인을 규칙화.
- **임신·육아 정보(추론)**: 산부인과·소아과에서 받은 안내문, 보건소 자료, 신뢰 기관 문서를 Gemini Notebook에 넣고 그 범위 안에서만 질문. 범용 챗봇의 의학 답변은 "진료 때 물어볼 질문 목록 만들기" 용도로 한정. 약·용량·응급 판단은 AI에 묻지 않는다.
- **관계·감정(추론)**: 배우자(민주)와의 대화를 AI에 "판정"시키지 않는다. 허용 범위는 ① 내 감정을 글로 정리하기(일기), ② 말하기 전에 표현을 다듬기, ③ 대화 후 내 몫의 개선점 찾기. AI는 사용자 편을 들기 쉬워(Stanford의 '조장' 사례) 갈등을 키울 수 있다는 점을 가족 규칙으로 명문화.
- **가족 사진(미확인)**: 구글 포토의 자연어 검색(Ask Photos) 등 AI 정리 기능은 공식 페이지 확인에 실패해 **[미확인]**. 어떤 서비스든 아이 얼굴·위치 데이터의 학습·공유 설정을 먼저 확인.

### Gaps
- 임신·육아 Q&A에 대한 LLM 정확도의 **한국어** 연구 미확보.
- Google Photos 'Ask Photos'·가족 사진 정리 AI의 2026 현황 **[미확인]**(404).
- AI 식단·여행 계획 도구의 효과를 다룬 2025–2026 자료 없음(위 내용은 커넥터 기능에서의 추론).

---

## 결론 산출물 — (1) 도구 선택표 (2) 주간 AI 루틴 초안 (3) 금지/주의 규칙 5개

### (1) 도구 선택표

| 용도 | 1순위 도구 | 대안 | 비용(확인된 범위) | 근거 |
|---|---|---|---|---|
| 제안서·견적서·후속 메일 초안 | Claude Projects + Skills(xlsx 생성) + Gmail 커넥터 | ChatGPT **[2026 요금 미확인]** | Claude Pro 이상(Skills 요건) | [Skills](https://claude.com/blog/skills), [커넥터](https://support.claude.com/en/articles/10166901) |
| 아침 브리핑·주간 리포트 자동화 | Claude Code Routines(예약 트리거) | Desktop 로컬 예약 작업 / Zapier | 구독 사용량 차감, 추가 요금 없음 | [Routines](https://code.claude.com/docs/en/routines) |
| 상권·점포 데이터 분석·리포트 게시 | Claude Code 클라우드 세션 + GitHub Pages(기존) | Google Sheets + Drive 커넥터 | Pro/Max 포함 | [클라우드 세션](https://code.claude.com/docs/en/claude-code-on-the-web) |
| 가맹본부 자료·계약서 질의(출처 고정) | Gemini Notebook(무료: 노트북 100·소스 50) | Claude Projects(RAG 모드) | 무료 | [플랜](https://support.google.com/gemininotebook/answer/16213268?hl=en) |
| 고객 미팅 녹취·회의록(한국어 화자분리) | 클로바노트(무료 한도 내) **[한도 미확인]** | 다글로 Pro $11.66/월(화자 5명) / 티로 Pro | 0 ~ $11.66/월 | [daglo](https://daglo.ai/), [tiro](https://tiro.ooo/) |
| 톡채널 고객 자동응답·예약 접수 | 카나나 상담매니저 | 외주 챗봇(크몽 등) | 요금 미기재(챗봇 일반요금 무료화 보도) | [카카오](https://www.kakaocorp.com/page/detail/11719) |
| 플랫폼 간 자동화(주문→시트 등) | Zapier Free(100태스크/월) | Make Free(1,000크레딧) / n8n Starter €20 | 0 ~ €20/월 | [Zapier](https://zapier.com/pricing), [Make](https://www.make.com/en/pricing), [n8n](https://n8n.io/pricing) |
| 신발 제품 사진(배경·그림자·일괄) | Photoroom Pro | Canva AI **[미확인]** | 연납 기준 요금(USD 미표기), 체험 가능 | [Photoroom](https://www.photoroom.com/pricing) |
| 인테리어 제안 시각화(상업공간) | ReimagineHome(무료 5장→Pro) | Midjourney/Flux **[미확인]** | 무료 5장, Pro 가격 별도 | [ReimagineHome](https://www.reimaginehome.ai/) |
| 골프 약점 진단(라운드 데이터) | Arccos(센서 $249.99 + 연회비 미확인) | 스코어 앱 수기 기록 | $249.99~ | [Arccos](https://www.arccosgolf.com/) |
| 골프 스윙 영상 분석 | Sportsbox 3D Golf(무료 5스윙/월 → $9.16/월) | V1 Golf / HackMotion($275~, 손목 문제 확인 시) | 0 ~ $9.16/월 | [Sportsbox](https://www.sportsbox.ai/), [HackMotion](https://hackmotion.com/) |
| 가족 일정·식단·여행 | Claude + Google Calendar 커넥터(가족 캘린더 분리) | Gemini(Workspace) **[미확인]** | Claude 플랜 포함 | [커넥터](https://support.claude.com/en/articles/10166901) |
| 임신·육아 정보 정리 | Gemini Notebook(병원·기관 자료만 소스로) | — (범용 챗봇은 질문 목록용) | 무료 | KQ8 연구 결과 |

### (2) 주간 AI 루틴 초안

- **매일 07:07 — 아침 브리핑(Routine, 읽기 전용)**: Gmail·Calendar 커넥터로 "오늘 일정 / 답장 없는 가맹 문의 / 어제 스마트스토어 주문 요약"을 아티팩트 페이지에 갱신. 발송·수정 금지 프롬프트. 읽는 시간 10분 고정, 알림은 이 시간에만. (근거: Routines 정각 지연 회피 권장, 커넥터 자율 실행 특성)
- **업무 중 — 초안 위임 블록(하루 2회, 각 25분)**: 제안서·견적서·블로그·후속 메일을 Projects에서 생성 → 숫자·고유명사·법조문만 체크리스트로 검증. 경계 밖 과업(계약 조항 해석·입지 숫자 교차검증)은 AI에 "질문 목록"만 요청. (근거: Noy&Zhang·Dell'Acqua)
- **현장·미팅 후 — 녹취 요약**: 사전 고지 후 클로바노트/다글로 녹음 → 요약·액션아이템을 가명화해 Projects에 저장 → 원본 30일 내 삭제.
- **매일 18:30 — 저녁 로그(5분)**: GitHub Pages 저장소 마크다운에 "오늘 AI에 맡긴 일 / 검토에 쓴 시간 / 틀린 것 1개"를 기록(Claude Code 세션에서 바로 커밋). 이것이 주간 리뷰의 원자료.
- **수요일 — 신발·메디쏠라 블록**: 판매 시트(Drive)로 "사이즈별 품절 위험·재주문 후보" 분석 1회, 리뷰 답글·상품 문안 생성, Photoroom 일괄 처리.
- **금요일 16:07 — 주간 리뷰(Routine + 사람)**: Routine이 저녁 로그 5일치를 요약해 "AI 덕에 줄인 시간 / 검토에 쓴 시간 / 틀린 사례"를 집계 → 사장님이 (a) 다음 주 AI에 맡길 과업 3개, (b) 맡기지 않을 과업 1개를 정함. 월 1회는 타이머로 동일 과업 AI 유/무 실측. (근거: METR의 체감–실측 괴리, Upwork의 검토 39%)
- **일요일 저녁 — 가족 블록(15분)**: 가족 캘린더로 다음 주 충돌·빈 저녁 2개 찾기, 주간 식단·장보기 목록 생성. 업무 계정과 분리된 커넥터만 사용.
- **골프(라운드 후)**: Arccos/스코어 데이터와 Sportsbox 영상 메모를 Projects에 올리고 "연습 과제 1개"만 받기. 월 1회 사람 코치 검수.

### (3) 금지/주의 규칙 5개

1. **출처 없는 숫자·날짜·법조문·고유명사는 문서에 넣지 않는다.** AI 출력에 링크를 요구하고 원문을 1회 연다(Dell'Acqua의 과신 메커니즘, Lee 외의 신뢰–비판적 사고 역관계).
2. **고객·거래처·가족의 식별정보를 원문 그대로 입력하지 않는다.** 가명화 후 입력, 주민번호·계좌번호 입력 금지, Pro/Max 학습 설정 OFF, 녹취는 사전 고지 + 30일 내 원본 삭제(개인정보위 2026.5 가이드, Anthropic 소비자 정책).
3. **자동 실행(Routines)에는 "발송·결제·삭제" 권한을 주지 않는다.** 초안·요약·게시만 허용하고, 불필요한 커넥터는 라우틴에서 제거. 녹색 상태를 성공으로 믿지 말고 로그를 본다(Routines 문서).
4. **의료·법률·세무·계약·관계 문제는 AI가 결론을 내지 않는다.** 임신·육아·약 복용은 의료진, 계약·권리금은 전문가, 부부 문제는 대화로 — AI는 질문 목록·표현 다듬기·기록 정리까지만(2026 의료 LLM 정확도 편차, Stanford 치료 챗봇 연구).
5. **"더 할 수 있다"는 이유로 업무 범위를 넓히지 않는다.** AI가 줄인 시간의 사용처를 주간 리뷰에 기록하고, 월 1회 실측 없이 AI 투입을 늘리지 않으며, 야간 알림은 끈다(METR 체감–실측 괴리, Upwork 77%).
