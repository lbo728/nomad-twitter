### 목차
[필요 페이지](##-필요-페이지)
[상세 기능 명세](##-상세-기능-명세)
[참고 사항](##-참고-사항)

# 기능 명세서

## 필요 페이지

- ‘/’: 로그인 여부를 확인하여 로그인이 되어있다면 홈페이지를 그렇지 않다면 계정 생성 / 로그인 페이지로 이동
- ‘/create-account’: 계정을 생성하는 페이지
- ‘/log-in’: 로그인을 진행하는 페이지
- ‘/tweet/[id]: 트윗의 상세 정보를 보는 페이지


## 상세 기능 명세

### /(홈 페이지)

- [ ]  (로그인한 후) 홈 페이지에서 사용자는 데이터베이스의 모든 트윗을 볼 수 있어야 한다.
- [ ]  (로그인한 후) 홈 페이지에서 사용자는 트윗을 게시(작성)할 수도 있어야 한다.

### /tweet/[id]

- [ ]  사용자는 id에 해당하는 트윗의 내용과 `좋아요` 버튼을 볼 수 있어야 한다.
- [ ]  `좋아요`버튼을 클릭했 을 경우 좋아요의 상태값이 데이터베이스에 저장되어야 하며 `useSWR`의 `mutate`를 사용하여 업데이트를 반영해야 합니다.


## 참고사항

- 챌린지 blueprint에는 `SQLite`을 기반으로 한 `Prisma`가 설정되어있습니다.
- `prisma.schema`파일을 변경했다면 `npm run db-sync`를 실행하세요.
- `SWR`와 `tailwind`도 챌린지 blueprint에 설정되어 있습니다.