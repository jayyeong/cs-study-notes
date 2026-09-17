# 여러 컴퓨터에서 이어서 공부하기

공용 기준은 이 GitHub 저장소의 파일입니다. Notion은 원본 자료, GitHub는 재작성한 학습자료와 진행 기록으로 사용합니다. 대화에만 남긴 결정은 다른 환경에서 필요한 문맥으로 활용하기 어려우므로 파일에도 기록합니다.

## 새 컴퓨터에서 처음 사용

Git이 설치된 터미널에서 실행합니다.

```sh
git clone https://github.com/jayyeong/cs-study-notes.git
cd cs-study-notes
```

그 폴더를 작업 폴더로 열고 아래처럼 요청합니다.

```text
README.md, AGENTS.md, progress.md를 읽고 현재 학습 상태를 파악해줘.
네트워크 모의면접 세트 A를 한 질문씩 진행하고,
끝나면 실제 답변에 근거해 복습 기록을 갱신해줘.
```

AGENTS.md는 프로젝트에 적용할 지침을 저장하는 파일입니다. 파일의 위치와 범위에 따라 적용되는 지침이 달라질 수 있습니다. [공식 AGENTS.md 안내](https://developers.openai.com/codex/guides/agents-md/)

## 공부 시작할 때

```sh
git status
git pull --ff-only
```

미커밋 변경이 있거나 pull이 실패하면 내용을 확인하고 정리합니다. 양쪽 컴퓨터에서 서로 다른 커밋이 생겨 fast-forward가 불가능하면 변경을 비교해 병합해야 합니다. 강제 덮어쓰기하지 않습니다.

## 공부를 마칠 때

예를 들어 진행 기록만 수정했다면:

```sh
git diff
git add progress.md
git commit -m "docs: record network review progress"
git push
```

다른 문서를 바꿨다면 그 파일만 추가합니다. 처음 push할 때는 해당 컴퓨터의 GitHub 인증이 필요할 수 있습니다. 내려받기는 공개 저장소라 인증 없이 가능하지만 게시 권한은 별개입니다. GitHub 토큰을 Markdown 파일이나 대화에 붙여 넣지 않습니다.

Git은 클라우드 폴더처럼 실시간 자동 동기화되지 않습니다. 컴퓨터를 바꾸기 전에 push, 다른 컴퓨터에서 시작하기 전에 pull하는 습관을 유지합니다. [GitHub 동기화 안내](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository)

## Notion 자료가 늘어났을 때

```text
sources/README.md의 기준 Notion 페이지에서 새로 추가된 운영체제 자료를 확인해줘.
접근 가능한 원본과 공식 문서를 바탕으로 학습자료와 면접 질문을 작성해줘.
출처, 확인일, 미수집 항목을 기록하고 curriculum.md와 progress.md를 갱신해줘.
공개 저장소에는 재작성한 자료만 넣어줘.
```

Notion 연결 상태와 원본 접근 권한은 사용하는 환경에서 확인해야 합니다. Git 저장소에 Notion 인증 정보를 넣어서 연결을 공유하지 않습니다.

## 자료 확장 규칙

- 학습 문서: study/os, study/database, study/backend 아래에 주제별 추가
- 면접 문서: interview 아래에 범위별 추가
- 새 주제 형식: [templates/topic.md](../templates/topic.md)
- 실제 학습 결과: [progress.md](../progress.md)
- 참고자료와 수집 제한: [sources/README.md](../sources/README.md)

현재 자동 스케줄, Notion 자동 수집, Git 자동 push는 설정하지 않았습니다.
