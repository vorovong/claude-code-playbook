# Claude Code Playbook

비개발자가 클로드 코드(Claude Code)로 업무 자동화를 배우는 학습 환경.

코딩을 몰라도 한국어로 대화하면서, 반복 업무를 자동화하는 프로젝트를 직접 만들 수 있다.

---

## 이게 뭔가요?

ChatGPT나 Claude 같은 챗봇은 **"답"** 을 준다.

클로드 코드는 다르다 — 대화로 컴퓨터에게 **직접 일을 시킨다.**
파일을 만들고, 코드를 작성하고, 자동화를 실행한다.

이 플레이북을 설치하면 클로드 코드가 **선생님 모드**로 바뀐다.
모든 걸 설명하면서 함께 프로젝트를 만들어주고,
경험이 쌓이면 점차 안내를 줄여간다.

---

<br>

# 시작하기

## 준비물

| 필요한 것 | 설명 |
|---|---|
| **컴퓨터** | Mac 또는 Windows |
| **Claude 구독** | Pro($20/월) 또는 Max($100/월). 무료 플랜은 불가. |

> 👉 아직 구독이 없다면: [claude.com/pricing](https://claude.com/pricing) 에서 가입

<br>

> ⚡ **진행 중 막히면?**
>
> 브라우저에서 [claude.ai](https://claude.ai) 채팅창을 **미리 열어두고** 아래 과정을 진행하세요.
> 에러가 나오면 그 내용을 복사해서 Claude 채팅에 붙여넣고 "이게 뭐야?" 하면 해결 방법을 알려줍니다.
>
> 이 방법은 설치 과정뿐 아니라, 앞으로 클로드 코드를 쓰면서 **언제든** 쓸 수 있습니다.

<br>

---

## 1단계: 터미널 열기

터미널은 글자로 컴퓨터에게 명령을 내리는 창이다.
카카오톡 대화창처럼 생겼는데, 상대방이 컴퓨터인 셈이다.

**Warp**(무료 터미널 앱)을 추천한다. 보기 편하고 회원가입 없이 바로 쓸 수 있다.

1. [warp.dev/download](https://www.warp.dev/download) 접속
2. 본인 컴퓨터에 맞는 버전 다운로드 (Mac / Windows)
3. 설치 후 실행

<details>
<summary>Warp 없이 기본 터미널로 하고 싶다면</summary>

- **Mac**: `Cmd + 스페이스바` → "터미널" 검색 → 열기
- **Windows**: `Win 키` → "PowerShell" 검색 → **"Windows PowerShell"** 열기

</details>

> 💡 Claude Desktop App에도 Code 탭이 있지만, 터미널(CLI)을 쓰는 게 **자유도가 훨씬 높다.** 처음부터 터미널에 익숙해지는 걸 추천한다.

---

## 2단계: Git 설치

Git은 "되돌리기"가 무한으로 되는 저장 시스템이다.
클로드 코드가 작업을 저장할 때 이걸 사용한다.

### Mac

터미널에 아래를 입력하고 `Enter`:

```
git --version
```

- 버전 번호가 나오면 → **이미 설치되어 있다.** 3단계로.
- 팝업이 뜨면 → **"설치"** 클릭. 몇 분 걸린다.

### Windows

터미널에 아래를 입력하고 `Enter`:

```
winget install --id Git.Git -e --source winget
```

설치 후 **Warp를 닫았다가 다시 연다.**

> 왜 닫았다 다시 여느냐면: 방금 설치한 프로그램을 인식하려면 터미널을 새로 열어야 한다. 한 번만 하면 된다.

---

## 3단계: 클로드 코드 설치

### Mac

```
curl -fsSL https://claude.ai/install.sh | bash
```

### Windows

```
irm https://claude.ai/install.ps1 | iex
```

- 영어로 뭔가 주르륵 나온다. 정상이다.
- 글자가 멈추면 설치 완료.
- **Warp를 닫았다가 다시 연다.**

---

## 4단계: 플레이북 설치 + 실행

아래를 **통째로** 복사 → 터미널에 붙여넣기 → `Enter`.

### Mac

```
mkdir -p ~/projects && git clone https://github.com/vorovong/claude-code-playbook.git ~/projects/claude-code-playbook && cd ~/projects/claude-code-playbook && claude
```

### Windows

```
mkdir -Force "$HOME\projects" | Out-Null; git clone https://github.com/vorovong/claude-code-playbook.git "$HOME\projects\claude-code-playbook"; cd "$HOME\projects\claude-code-playbook"; claude
```

> 이 한 줄이 하는 일:
> 프로젝트 폴더 만들기 → 플레이북 다운로드 → 이동 → 클로드 코드 실행

---

## 5단계: 로그인 (최초 1회)

처음 실행하면 몇 가지 질문이 나온다.

| 질문 | 선택 |
|---|---|
| 텍스트 스타일 | 아무거나 골라서 `Enter` |
| 로그인 방법 | **"Claude account with subscription"** |
| 브라우저 로그인 | `Enter` → 브라우저에서 Claude에 로그인 |
| 폴더 신뢰 | **"Yes, proceed"** |

---

## 6단계: 대화 시작!

`>` 표시가 나오면 준비 완료.

### 👉 "안녕하세요" 라고 입력하고 `Enter`

클로드가 이름을 물어보고, 어떤 업무를 자동화하고 싶은지 대화를 시작한다.
30분 안에 첫 결과물을 함께 만들게 된다.

잘 모르겠으면 "잘 모르겠어요"라고 해도 된다. 클로드가 쉽게 다시 설명해준다.

---

<br>

# 그 다음은?

## 다시 시작하려면

다음에 이어서 할 때, 터미널(Warp)을 열고 아래를 붙여넣으면 된다.

**Mac:**
```
cd ~/projects/claude-code-playbook && claude
```

**Windows:**
```
cd "$HOME\projects\claude-code-playbook"; claude
```

클로드가 지난번 상황을 기억하고 이어서 안내해준다.

> 💡 명령어가 기억나지 않으면, 터미널에서 `↑`(위 화살표)를 누르면 이전 명령어가 나온다.

---

## 막히면

1. 에러 메시지를 **복사**한다
2. [claude.ai](https://claude.ai) 채팅에 **붙여넣는다**
3. "이 에러가 뭐야?"라고 물어본다
4. 해결 방법을 터미널에 다시 붙여넣는다

> 💡 **터미널 기본 조작**
> | 상황 | 방법 |
> |---|---|
> | 잘못 입력해서 멈춤 | `Ctrl + C` 누르면 취소 |
> | 비밀번호 입력 시 글자 안 보임 | 정상이다 (보안 기능). 그냥 입력 후 `Enter` |
> | 클로드 코드 종료 | `Ctrl + C` 또는 `/exit` 입력 |

---

## 온라인에 저장하기 (나중에)

처음에는 내 컴퓨터에만 저장된다.
나중에 온라인(GitHub)에도 백업하고 싶으면, 클로드 코드에게 이렇게 말하면 된다:

> "내 프로젝트를 GitHub에 올리고 싶어. 도와줘."

클로드가 가입부터 저장까지 안내해준다.

---

<br>

# 플레이북 상세

## Phase 시스템

클로드의 안내 수준이 경험에 따라 자동으로 바뀐다.

| Phase | 모드 | 설명 |
|---|---|---|
| 1 | 교사 | 모든 것을 설명. 단계마다 멈추고 안내한다. |
| 2 | 코치 | 핵심만 안내. 사용자가 의사결정을 주도한다. |
| 3 | 협업자 | 사용자 주도. 사용자가 설계하고 클로드가 실행한다. |

## 미니 → 풀 프로젝트

| | 미니 프로젝트 | 풀 프로젝트 |
|---|---|---|
| 시기 | Phase 1~2 | Phase 2~3 |
| 위치 | 이 플레이북 안에서 | 별도 프로젝트 폴더 |
| 규모 | 단순 자동화 연습 | 복합 자동화, AI 환경 설계 |

## 폴더 구조

```
claude-code-playbook/
├── CLAUDE.md           ← 클로드의 행동 규칙 (핵심)
├── README.md           ← 지금 읽고 있는 파일
├── mini-projects/      ← 미니 프로젝트 결과물
├── progress/           ← 학습 진행 기록
└── docs/
    ├── guides/         ← 가이드 문서
    ├── templates/      ← 문서 양식
    └── case-studies/   ← 완료된 프로젝트 후기
```

## 커스텀하기

이 플레이북은 **출발점**이지 완성품이 아니다.
프로젝트를 진행하면서 CLAUDE.md를 고치고, 자기만의 패턴을 만들고,
풀 프로젝트에서 독립적인 AI 환경을 설계하게 된다.
커스텀하는 과정 자체가 학습이다.

---

## 기여하기

- 시스템 개선 아이디어 → [Issue](https://github.com/vorovong/claude-code-playbook/issues)
- 직접 개선 → PR
- 개인 프로젝트 결과물은 각자의 레포에서 관리

## 라이선스

[MIT](LICENSE)
