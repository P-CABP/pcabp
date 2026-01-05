# Work Management

작업 내역의 관리 방법에 대한 convention 입니다.

### GitHub Project

- GitHub Project 를 통해서 작업 내역에 대한 ticket 들을 관리합니다.
- https://github.com/orgs/P-CABP/projects/1
- 작업을 위한 내용을 issue ticket 으로 생성하여 작업을 진행합니다.

### Issue Ticket

- Issue ticket 은 총 3개의 타입으로 분류됩니다.
- Task : 비즈니스와 관련 없이 프로젝트의 기능 개발을 위한 issue ticket 입니다.
- Feature : 비즈니스 업무 기능 개발을 위한 issue ticket 입니다.
- Bug : 오류가 발견되는 경우 오류 내용, 원인, 해결을 작성하는 오류 수정 issue ticket 입니다.

### Issue Ticket Content

- Issue ticket 을 생성하면 각 issue 별로 다른 template 이 생성됩니다.
- Template 에 맞게 내용을 작성합니다.
- Share Point 의 경우 optional 하게 작성하는 내용입니다.
  - 개발한 내용이 다른 개발자들에게도 공유가 되어야 하는 경우 Share Point 를 작성한 후 label 로 SP 를 추가합니다.
  - SP 가 붙은 ticket 에 대한 pull request 는 모든 개발자들이 확인합니다.
  - e.g. Pagination 을 처리하기 위한 usePagination 훅을 생성한 경우 다른 개발자들이 내용을 공유 받을 수 있도록 Share Point 에 작성합니다.
 
### Issue Ticket Process

- Issue ticket 의 진행상태는 Backlog, Ready, In progess, In review, Done 입니다.
- Blocked : Issue 내용을 작성중이거나 다른 사유로 인하여 작업이 불가능한 상태
- Ready : 바로 개발 진행이 가능한 상태
- Progress : 개발을 진행 중인 상태
- Review : PR 을 올린 상태
- Done : 완료한 상태




