# 부동산 실무 AI 활용 교육: Windows 설치 가이드

이 문서를 위에서부터 순서대로 따라 해 주세요.
명령어 상자에 마우스를 올리면 오른쪽 위에 복사 버튼이 나타납니다. 버튼이 보이지 않으면 명령어를 마우스로 드래그해 선택한 뒤 Ctrl+C로 복사해 주세요.

오늘 설치하는 프로그램은 3가지입니다.

- **Git for Windows**: Claude Code가 작업 명령을 실행할 때 쓰는 보조 프로그램입니다.
- **Claude Code**: 명령어 창에서 내 PC의 파일을 직접 읽고 쓰는 AI 도구입니다.
- **Orca**: 여러 AI 작업창을 한 화면에서 관리하는 프로그램입니다.

## 준비 3가지

1. **Claude 유료 요금제**: Pro 이상의 유료 요금제가 필요합니다. 무료 계정으로는 Claude Code를 사용할 수 없습니다.
2. **Windows 10 버전 1809 이상**: 시작 메뉴에서 `winver`를 입력하면 버전을 확인할 수 있습니다.
3. **PowerShell 여는 법**: PowerShell은 Windows에 기본으로 들어 있는 명령어 입력 창입니다. 시작 메뉴에서 PowerShell을 검색해 이름에 (x86)이 없는 것을 여세요. 창에 `PS C:\Users\이름>`처럼 표시되면 맞게 여신 것입니다.

**붙여넣기 방법**: PowerShell 창에서 마우스 오른쪽 버튼을 클릭하거나 Ctrl+V를 누른 뒤 Enter를 누르세요.

## 1단계: Git for Windows 설치

Git 사용법은 이번 교육에서 배우지 않습니다. 설치만 해 두시면 됩니다.

1. <https://git-scm.com/install/windows> 에 접속합니다.
2. **Git for Windows/x64 Setup**을 눌러 설치 파일을 받아 실행합니다.
3. 모든 화면에서 기본값 그대로 **Next**를 누릅니다.
4. 설치가 끝나면 PowerShell을 새로 열고 아래 명령을 실행합니다.

```powershell
git --version
```

`git version`으로 시작하는 글자가 보이면 성공입니다.

## 2단계: Claude Code 설치

PowerShell에서 아래 명령을 실행합니다. 관리자 권한은 필요 없습니다.

```powershell
irm https://claude.ai/install.ps1 | iex
```

다운로드 중에는 진행 표시가 없을 수 있습니다. 끝날 때까지 기다려 주세요. `Claude Code successfully installed!`가 보이면 설치가 끝난 것입니다.

PowerShell 창을 닫고 새로 연 뒤 아래 명령을 실행합니다.

```powershell
claude --version
```

버전 번호가 보이면 성공입니다.

## 3단계: Claude 로그인

PowerShell에서 아래 명령을 실행합니다.

```powershell
claude
```

1. 브라우저 창이 열리면 Claude 유료 구독 계정으로 로그인합니다.
2. 화면에 나오는 안내를 따른 뒤 PowerShell 창으로 돌아옵니다.
3. 입력창이 보이면 로그인이 끝난 것입니다.
4. 아래 내용을 입력해 Claude를 종료합니다.

```text
/exit
```

## 4단계: Orca 설치

공식 안내: <https://www.onorca.dev/docs/install>

아래 주소를 눌러 설치 파일을 받아 실행합니다. Orca라는 이름의 다른 프로그램이 많으니 반드시 이 주소만 사용해 주세요.

<https://github.com/stablyai/orca/releases/latest/download/orca-windows-setup.exe>

다운로드가 504 오류 등으로 실패하면 강사에게 말씀해 주세요. 비상용 설치 파일을 전달해 드립니다. Git for Windows도 같습니다.

Windows 보호 화면이 뜨면, 위 공식 주소에서 받은 파일에 한해 **추가 정보**를 누른 다음 **실행**을 누릅니다.

처음 실행하면 나오는 설정은 다음과 같이 해 주세요.

| 항목 | 설정 |
|---|---|
| 홈 폴더 접근 | 허용합니다. |
| 시스템에서 감지됨 | Claude Code가 목록에 있는지 확인합니다. |
| Yolo 모드 | 끕니다. AI가 승인 없이 실행하는 설정이라 교육 중에는 사용하지 않습니다. |
| 기본 셸 | PowerShell을 선택합니다. 셸은 명령어를 받아 실행하는 프로그램입니다. |
| 오른쪽 클릭 동작 | 오른쪽 클릭으로 붙여넣기를 선택합니다. |
| GitHub 연동 등 나머지 | 건너뛰어도 됩니다. |

## 5단계: 작업 폴더 열기

바탕화면의 빈 곳을 마우스 오른쪽 버튼으로 클릭하고 **새로 만들기**, **폴더** 순서로 눌러 폴더를 만듭니다. 폴더 이름은 영어로 `ai-class`라고 입력해 주세요.

Orca에서 다음 순서로 폴더를 엽니다. 화면이 영어이면 괄호 안의 이름을 찾아 주세요.

1. **프로젝트 추가(Add project)** 를 누릅니다.
2. **폴더 찾아보기(Browse folder)** 를 누릅니다.
3. 바탕 화면의 `ai-class` 폴더를 선택합니다.
4. "이 폴더는 Git repos가 아닙니다"라는 안내는 정상입니다. **폴더로 열기(Open as Folder)** 를 누릅니다.

Orca의 터미널(명령어를 입력하는 창)에 아래 내용을 입력합니다. 터미널이 보이지 않으면 실행 화면에서 Claude Code 또는 빈 터미널(Blank Terminal)을 선택해 주세요.

```text
claude
```

이 폴더를 신뢰하는지 물으면 승인합니다.

여기까지 되셨으면 설치가 끝났습니다. 이어서 [1회차 실습](01_실습.md)으로 넘어가 주세요.

## 막혔을 때

### 'irm'을 인식할 수 없다고 나올 때

PowerShell이 아니라 CMD 창에서 실행하신 경우입니다. PowerShell을 열고 2단계 명령을 다시 실행해 주세요.

### 'claude'를 인식할 수 없다고 나올 때

먼저 창을 닫고 새로 열어 다시 실행해 주세요. 그래도 안 되면 아래 명령을 실행합니다.

```powershell
Test-Path "$env:USERPROFILE\.local\bin\claude.exe"
```

`True`가 나오면 프로그램은 설치되었고 PATH(프로그램 위치를 찾는 목록)만 등록되지 않은 상태입니다. 아래 명령을 실행하고 창을 새로 열어 주세요.

```powershell
$currentPath = [Environment]::GetEnvironmentVariable('PATH', 'User')
[Environment]::SetEnvironmentVariable('PATH', "$currentPath;$env:USERPROFILE\.local\bin", 'User')
```

`False`가 나오면 설치가 끝나지 않은 것이니 2단계를 다시 진행해 주세요.

### TLS 또는 SSL 오류가 나올 때

주로 오래된 Windows 10에서 발생합니다. 아래 명령으로 다시 설치해 주세요.

```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
irm https://claude.ai/install.ps1 | iex
```

### 32-bit Windows를 지원하지 않는다고 나올 때

이름에 (x86)이 붙은 PowerShell을 여신 경우입니다. (x86)이 없는 PowerShell을 열어 다시 실행해 주세요.

### 설치 명령이 HTML을 돌려주거나 다른 방법이 필요할 때

아래 명령으로 설치할 수 있습니다. 이 방법으로 설치하면 자동 업데이트가 되지 않습니다.

```powershell
winget install Anthropic.ClaudeCode
```

### 회사망 또는 프록시 오류가 나올 때

직접 해결하지 마시고 강사에게 문의해 주세요.

## 2회차 과제: Python 설치

Python은 엑셀 파일 작성과 데이터 수집에 쓰는 프로그램입니다. 2회차 전까지 설치해 주세요.

1. Microsoft Store에서 Python 공식 install manager(설치 관리 도구)를 설치합니다: <https://apps.microsoft.com/detail/9NQ7512CXL7T>
2. Store가 막혀 있으면 이 파일을 받아 설치합니다: <https://www.python.org/ftp/python/pymanager/python-manager-26.4.msix>
3. PowerShell을 새로 열고 아래 명령을 실행합니다.

```powershell
python
```

4. 런타임(Python 실행 파일) 설치나 PATH 추가를 물으면 동의합니다.
5. `>>>`가 보이면 아래 내용을 입력해 종료합니다.

```text
exit()
```

6. 아래 명령을 실행해 설치된 Python이 목록에 나오면 완료입니다.

```powershell
py list
```

## 2회차 실습

[2회차 실습](02_실습.md)

## 공식 문서

- [Claude Code 설치](https://code.claude.com/docs/en/setup)
- [Claude Code 설치 문제 해결](https://code.claude.com/docs/en/troubleshoot-install)
- [Claude Code 터미널 입문 안내](https://code.claude.com/docs/en/terminal-guide)
- [Orca 설치](https://www.onorca.dev/docs/install)
- [Git for Windows](https://git-scm.com/install/windows)
- [Python Windows 사용 안내](https://docs.python.org/3/using/windows.html)
