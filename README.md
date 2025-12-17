# wlab-claude-code-marketplace

Wondermove에서 관리하는 Claude Code 플러그인 마켓플레이스입니다.

## 구조

```
.claude-plugin/
  marketplace.json       # 마켓플레이스 메타데이터
plugins/
  commit-commands/       # Git 커밋 워크플로우 플러그인
    .claude-plugin/
      plugin.json        # 플러그인 메타데이터
    commands/
      commit.md          # 커밋 생성 명령어
      clean_gone.md      # [gone] 브랜치 정리 명령어
```

## 플러그인 목록

### commit-commands (v1.0.0)

Git 커밋 워크플로우를 위한 명령어 모음입니다.

| 명령어                        | 설명                                     |
| ----------------------------- | ---------------------------------------- |
| `/commit-commands:commit`     | 현재 변경사항으로 git commit 생성        |
| `/commit-commands:clean_gone` | 원격에서 삭제된 로컬 브랜치([gone]) 정리 |

## 마켓플레이스 등록

이 마켓플레이스를 Claude Code에 등록하려면:

```bash
claude marketplace add https://github.com/Wondermove-Inc/wlab-claude-code-marketplace.git
```

## 플러그인 설치

마켓플레이스 등록 후 플러그인을 설치하려면:

```bash
claude plugin install <plugin-name> --from wlab-claude-code-marketplace
```

예시:

```bash
claude plugin install commit-commands --from wlab-claude-code-marketplace
```

## 새 플러그인 추가

1. `plugins/` 디렉토리에 새 플러그인 폴더 생성
2. `.claude-plugin/plugin.json` 파일 작성
3. `marketplace.json`에 플러그인 등록

## 라이선스

Wondermove 내부 사용
