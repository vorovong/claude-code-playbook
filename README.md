# Claude Code Playbook

비개발자가 클로드 코드(Claude Code)를 배우는 단계별 학습 환경.

코딩을 몰라도 한국어로 대화하면서, 반복 업무를 자동화하는 프로젝트를 직접 만들어볼 수 있다.

---

## 이게 뭔가요?

ChatGPT나 Claude 같은 챗봇은 "답"을 준다. 클로드 코드는 다르다 — 대화로 컴퓨터에게 **직접 일을 시킨다.** 파일을 만들고, 코드를 작성하고, 자동화를 실행한다.

이 플레이북은 클로드 코드를 처음 쓰는 사람을 위한 학습 환경이다. 설치하고 실행하면, 클로드가 선생님처럼 안내하면서 함께 프로젝트를 만들어준다.

경험이 쌓이면 안내 수준이 줄어들고(Phase 전환), 나중에는 복잡한 자동화를 직접 설계하게 된다.

---

## 시작하기

### 준비물

- **컴퓨터** (Mac 또는 Windows)
- **Claude 구독** (Pro $20/월 또는 Max $100/월) — [claude.com/pricing](https://claude.com/pricing)에서 가입
  - 이미 Claude를 유료로 쓰고 있다면 추가 비용 없다.
  - 무료 플랜으로는 클로드 코드를 사용할 수 없다.

---

### 1단계: 터미널 준비

터미널은 글자로 컴퓨터에게 명령을 내리는 창이다. 카카오톡 대화창처럼 생겼는데, 상대방이 컴퓨터인 셈이다.

**Warp**(무료 터미널 앱)을 추천한다. 보기 편하고 회원가입 없이 바로 사용 가능하다.

1. [warp.dev/download](https://www.warp.dev/download) 에 접속
2. 본인 컴퓨터에 맞는 버전을 다운로드 (Mac / Windows)
3. 설치 후 실행

> 💡 **Claude Desktop App**(데스크톱 앱)을 이미 쓰고 있다면, 앱 안의 **Code 탭**에서도 클로드 코드를 사용할 수 있다. 이 경우 Warp 설치 없이 바로 2단계로 넘어가도 된다. 다운로드: [claude.com/download](https://claude.com/download)

<details>
<summary>Warp 없이 기본 터미널로 하고 싶다면 (클릭해서 펼치기)</summary>

**Mac:** `Cmd + 스페이스바` → "터미널" 검색 → 열기
**Windows:** `Win 키` → "PowerShell" 검색 → **"Windows PowerShell"** 열기

</details>

---

### 2단계: Git 설치

Git은 파일의 변경 이력을 기록하는 도구다. "되돌리기"가 무한으로 되는 저장 시스템이라고 생각하면 된다. 클로드 코드가 작업을 저장할 때 이걸 사용한다.

터미널(Warp)에서 아래를 복사해서 붙여넣고 `Enter`:

**Mac의 경우:**
```
git --version
```
- 버전 번호가 나오면 (예: `git version 2.39.0`) → 이미 설치되어 있다. 다음 단계로.
- "설치하시겠습니까?" 같은 팝업이 뜨면 → **"설치"** 클릭. 몇 분 걸린다.

**Windows의 경우:**
```
winget install --id Git.Git -e --source winget
```
- 설치가 끝나면 **Warp를 닫았다가 다시 열어야 한다.**

> 왜 닫았다 다시 여느냐면: 방금 설치한 프로그램을 컴퓨터가 인식하려면 터미널을 새로 열어야 한다. 한 번만 하면 된다.

---

### 3단계: 클로드 코드 설치

터미널(Warp)에서 아래를 복사해서 붙여넣고 `Enter`:

**Mac의 경우:**
```
curl -fsSL https://claude.ai/install.sh | bash
```

**Windows의 경우:**
```
irm https://claude.ai/install.ps1 | iex
```

- 영어로 뭔가 주르륵 나온다. 정상이다. 설치가 진행 중인 것이다.
- 글자가 멈추면 설치 완료.
- **Warp를 닫았다가 다시 연다.** (같은 이유)

---

### 4단계: 플레이북 설치 + 실행

여기가 마지막이다. 아래를 **통째로** 복사해서 붙여넣고 `Enter`:

**Mac의 경우:**
```
mkdir -p ~/projects && git clone https://github.com/vorovong/claude-code-playbook.git ~/projects/claude-code-playbook && cd ~/projects/claude-code-playbook && claude
```

**Windows의 경우:**
```
mkdir -Force "$HOME\projects" | Out-Null; git clone https://github.com/vorovong/claude-code-playbook.git "$HOME\projects\claude-code-playbook"; cd "$HOME\projects\claude-code-playbook"; claude
```

이 명령어가 하는 일:
1. 프로젝트 폴더를 만든다
2. 플레이북을 다운로드한다
3. 그 폴더로 이동한다
4. 클로드 코드를 실행한다

---

### 5단계: 로그인 (최초 1회)

처음 실행하면 몇 가지 질문이 나온다.

1. **텍스트 스타일**: 화살표로 아무거나 골라서 `Enter`
2. **로그인 방법**: **"Claude account with subscription"** 선택
3. **브라우저 로그인**: `Enter` 누르면 브라우저가 열린다. 평소처럼 Claude에 로그인
4. **폴더 신뢰**: "Yes, proceed" 선택

---

### 6단계: 대화 시작

`>` 표시가 나오면 준비 완료다.

**"안녕하세요"라고 입력하고 `Enter`를 누르면 대화가 시작된다.**

클로드가 이름을 물어보고, 어떤 업무를 자동화하고 싶은지 대화를 시작한다. 30분 안에 첫 결과물을 함께 만들게 된다.

어렵게 느껴지면 언제든 "잘 모르겠어요"라고 말해도 된다. 클로드가 다시 쉽게 설명해준다.

---

## 다시 시작하려면

다음에 다시 이어서 하고 싶을 때, 터미널(Warp)을 열고 아래를 붙여넣으면 된다:

**Mac:**
```
cd ~/projects/claude-code-playbook && claude
```

**Windows:**
```
cd "$HOME\projects\claude-code-playbook"; claude
```

클로드가 지난번 진행 상황을 기억하고 이어서 안내해준다.

> 💡 **팁**: 이 명령어가 기억나지 않으면, 터미널에서 위 화살표(`↑`)를 누르면 이전에 입력한 명령어가 나온다.

---

## 막히면 어떻게 하나

터미널에서 영어 에러가 나와도 당황하지 않아도 된다.

1. **에러 메시지를 복사한다** (드래그로 선택 → `Cmd+C` 또는 `Ctrl+C`)
2. **[claude.ai](https://claude.ai)에 붙여넣는다** (브라우저에서 Claude 채팅)
3. "이 에러가 뭔지 알려줘"라고 물어본다
4. Claude가 해결 방법을 알려주면, 터미널에 다시 붙여넣는다

> 💡 **터미널 기본 조작**:
> - 뭔가 잘못 입력해서 멈춰 있으면 → `Ctrl + C`를 누르면 취소된다
> - 비밀번호를 입력하는데 글자가 안 보이는 건 정상이다 (보안 기능)
> - `Ctrl + C`로 클로드 코드를 종료할 수 있다

---

## 이 플레이북이 하는 일

### Phase 시스템 — 클로드의 안내 수준이 바뀐다

| Phase | 역할 | 설명 |
|---|---|---|
| Phase 1: 교사 | 모든 것을 설명 | 처음 시작하는 사람. 단계마다 멈추고 설명한다. |
| Phase 2: 코치 | 핵심만 안내 | 미니 프로젝트 2~3개 완료. 사용자가 의사결정을 주도한다. |
| Phase 3: 협업자 | 사용자 주도 | 독립 프로젝트 진행. 사용자가 설계하고 클로드가 실행한다. |

### 미니 프로젝트 → 풀 프로젝트

```
미니 프로젝트 (Phase 1~2)          풀 프로젝트 (Phase 2~3)
------------------------------     --------------------------------
- 이 플레이북 안에서 진행            - 별도 프로젝트 폴더로 독립
- 단순하고 빠른 자동화 연습          - 복합 자동화, AI 실행 환경 설계
- 결과물: mini-projects/ 에 저장     - 결과물: 별도 프로젝트 폴더에 저장
```

---

## 온라인에 저장하기 (나중에)

처음에는 내 컴퓨터에만 저장된다. 나중에 온라인(GitHub)에도 저장하고 싶으면, 클로드 코드에게 이렇게 말하면 된다:

> "내 프로젝트를 GitHub에 올리고 싶어. 도와줘."

클로드가 GitHub 가입부터 저장까지 안내해준다.

---

## 폴더 구조

```
claude-code-playbook/
  CLAUDE.md                    -- 클로드의 행동 규칙 (이 프로젝트의 핵심)
  README.md                    -- 지금 읽고 있는 파일
  mini-projects/               -- 미니 프로젝트 결과물
  progress/                    -- 학습 진행 기록
  docs/
    guides/                    -- 가이드 문서
    templates/                 -- 문서 양식
    case-studies/              -- 완료된 프로젝트 후기
```

---

## 커스텀하기

이 플레이북은 **출발점**이지 완성품이 아니다. 프로젝트를 진행하면서 CLAUDE.md를 고치고, 자기만의 패턴을 만들고, 풀 프로젝트에서 독립적인 AI 환경을 설계하게 된다. 커스텀하는 과정 자체가 학습이다.

---

## 기여하기

- 시스템 개선 아이디어 → [Issue](https://github.com/vorovong/claude-code-playbook/issues)
- 직접 개선 → PR
- 개인 프로젝트 결과물은 각자의 레포에서 관리

---

## 라이선스

[MIT](LICENSE)
