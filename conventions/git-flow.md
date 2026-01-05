# Git

### Git Strategy

- P-CABP 에서는 Git Flow 전략을 사용합니다.
- 각각의 [issue ticket](https://github.com/P-CABP/pcabp/blob/main/conventions/work.md) 은 하나의 branch 와 연결됩니다.

### Branch Naming

- Branch 의 이름은 TYPE/FEATURE 으로 네이밍합니다.
- TYPE 은 다음과 같습니다.
  - feature : 기능 개발
  - bugfix : 오류 수정
  - refactor : 코드 리팩토링
  - style : 코드 포맷팅
  - docs : 문서 작업
  - chore : 설정 관련 작업
  - test : 테스트 코드
  - 추가적인 유형이 필요한 경우 논의 후 추가합니다.
- FEATURE 는 소문자 kebab-case 으로 자유롭게 작성하되 개발 내용이 충분히 포함되도록 합니다.

### Commit Message Naming

- Commit message 는 TYPE(SCOPE): DESCRIPTION 으로 작성합니다.
- TYPE 은 Branch 의 TYPE 과 동일하지만 bugfix 만 fix 으로 변경하여 작성합니다.
- SCOPE 은 optional 한 내용으로 domain, file, folder 등 특정 영역을 표현할 때 작성합니다.
- DESCRIPTION 은 영어/한글 자유롭게 작성이 가능하되 개발 내용이 충분히 포함되도록 합니다.

### Git Flow

Step 0. 기본 브랜치는 다음과 같이 존재합니다.
- main : 운영환경 브랜치입니다.
- develop : main 에서 파생된 개발환경 브랜치입니다.

Step 1. develop branch 에서 필요한 브랜치를 생성합니다.
- e.g. git switch develop && git switch -c feature/authentication

Step 2. 작업이 완료되면 PR 을 생성합니다.
- Target branch 는 develop branch 으로 설정합니다.
- 생성된 PR 은 Issue Ticket 과 연결합니다.
- PR 에는 issue ticket 의 링크과 간단한 설명을 작성합니다.
  - PR 에는 간단한 내용만 작성하기 때문에 issue ticket 에 최대한 자세하게 내용을 작성합니다.

Step 3. PR 에 대한 코드 리뷰를 요청합니다. (Slack code-review channel)
- PR 링크와 함께 리뷰 요청을 합니다. (Share Point 가 있는 경우 이를 명시합니다.)
- 개발자들은 코드 리뷰를 진행합니다.
  - 코드 리뷰를 완료한 경우 리뷰 요청 스레드에 댓글을 답니다.
  - PR 담당자는 리뷰 내용을 확인하여 대응합니다.
- 코드 리뷰에 대한 대응이 완료되면 리뷰한 개발자들은 승인을 합니다.
- 승인이 되면 PR 담당자는 병합을 진행합니다.
  - Share Point 가 있는 경우 모든 개발자들의 승인을 확인 후 병합합니다.

Step 4. PR 이 정상적으로 병합이 되면 develop branch 에서 테스트를 진행합니다.
- 테스트까지 완료되면 issue ticket 을 done 처리합니다.