# commit-commands

Git 커밋 워크플로우를 간소화하는 Claude Code 플러그인입니다.

## 설치

```bash
claude plugin install commit-commands --from wlab-claude-code-marketplace
```

## 명령어

### `/commit-commands:commit`

현재 변경사항을 기반으로 git commit을 생성합니다.

**기능:**

- 현재 git status 확인
- staged/unstaged 변경사항 분석
- 적절한 커밋 메시지 자동 생성
- 변경사항 스테이징 및 커밋

**사용 예시:**

```
/commit-commands:commit
```

### `/commit-commands:clean_gone`

원격에서 삭제된 로컬 브랜치(`[gone]`)를 정리합니다.

**기능:**

- `[gone]` 상태인 브랜치 탐지
- 연결된 worktree 자동 제거
- 브랜치 삭제

**사용 예시:**

```
/commit-commands:clean_gone
```

## 버전

- **현재 버전:** 1.0.0
