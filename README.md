# NodeZzang

| 메인페이지 | 상세페이지 |
|:-:|:-:|
| ![메인페이지](https://velog.velcdn.com/images/whdgnszz1/post/b98c5664-8673-418c-a35b-0faf27912f1e/image.png) | ![상세페이지](https://velog.velcdn.com/images/whdgnszz1/post/c0fe2156-5ecc-43e2-bf96-dd61beaa1ea4/image.png) |

| 채팅방 목록 | 채팅방 |
|:-:|:-:|
| ![채팅방 목록](https://velog.velcdn.com/images/whdgnszz1/post/f1c2403a-1e1c-4a46-9186-51dcf21c4b49/image.png) | ![채팅방](https://velog.velcdn.com/images/whdgnszz1/post/77566ce0-c356-4673-96b2-1039a0858bfc/image.png) |

| 프로필 페이지 | 프로필 수정 |
|:-:|:-:|
| ![프로필 페이지](https://velog.velcdn.com/images/whdgnszz1/post/45934317-2abd-4c17-8c86-bd4b1a703dff/image.png) | ![프로필 수정](https://velog.velcdn.com/images/whdgnszz1/post/c3cc7c74-4615-4c5d-8814-1a5477fad22e/image.png) |



### 프로젝트의 기능은 다음과 같습니다.

### 1. 회원가입
- 닉네임, 비밀번호를 사용하여 회원가입이 가능합니다.
- 이메일 입력칸이 추가될 예정입니다. ( 개발 중 )
- 로그인 시 닉네임 중복확인, 이메일 인증이 추가될 예정입니다. ( 개발 중 )

### 2. 로그인
- 닉네임, 비밀번호를 사용하여 로그인이 가능합니다.
- 로그인 시 accessToken과 refreshToken이 발급되며, 만료된 accessToken을 전달하면 accessToken이 갱신됩니다.
- 구글 로그인, 카카오 로그인이 추가될 예정입니다. ( 개발 중 )

### 3. 게시글
- 로그인한 사용자만 게시글 작성이 가능합니다.
- 로그인한 사용자만 댓글 작성이 가능합니다.
- 본인이 작성한 댓글만 수정, 삭제가 가능합니다.
- 좋아요를 누르면 오른쪽 하단의 하트모양의 색이 바뀝니다.

### 4. 채팅
- 로그인한 사용자만 채팅방 생성이 가능합니다.
- 채팅방 생성시 최소인원은 2명입니다.
- 채팅방에 비밀번호를 설정할 수 있습니다.
- 채팅방의 스크롤을 위로 올리면 과거의 채팅 내역을 추가로 받아오게 하는 기능이 추가될 예정입니다. ( 개발 중 )

### 5. 프로필
- 유저 프로필사진의 오른쪽 하단 연필모양 버튼을 클릭하면 프로필 사진, 닉네임 수정이 가능합니다.



# Sparta Node Assignment
![Swagger](https://velog.velcdn.com/images/whdgnszz1/post/ad016204-417a-4907-afb7-9695c2d9a11c/image.png)

## Level1.

</br>

### 프로젝트의 기능은 다음과 같습니다.
1. 게시글 생성
  - 게시글을 생성할 때 request의 body로 비밀번호를 설정합니다. 수정, 삭제시 일치하는 비밀번호로 요청해야 합니다.

2. 게시글 조회
  - /posts 엔드포인트로 전체 게시글 조회가 가능합니다.

3. 게시글 수정
  - request의 body에 게시글을 작성할 때 사용했던 비밀번호로 게시글을 수정할 수 있습니다.

4. 게시글 삭제
  - request의 body에 게시글을 작성할 때 사용했던 비밀번호로 게시글을 수정할 수 있습니다.

5. 댓글 생성
  - 댓글을 생성할 때 request의 body로 비밀번호를 설정합니다. 수정, 삭제시 일치하는 비밀번호로 요청해야 합니다.

6. 특정게시글의 댓글 조회
  - /posts/:postId/comments 엔드포인트로 특정게시글의 댓글 조회가 가능합니다.

7. 댓글 수정
  - request의 body에 댓글을 작성할 때 사용했던 비밀번호로 게시글을 수정할 수 있습니다.

8. 댓글 삭제
  - request의 body에 댓글을 작성할 때 사용했던 비밀번호로 게시글을 수정할 수 있습니다.

***
## Level2_Express

### Level2_Express에서 변경된 내용은 다음과 같습니다.
1. ODM을 사용했던 프로젝트를 ORM 프로젝트로 리팩토링 진행
  - Mongoose -> Prisma

***
## Level3_Express_sessionLogin

### Level3_Express_sessionLogin에서 변경된 내용은 다음과 같습니다.

1. 회원가입
  - nickname과 password로 회원가입이 가능합니다.

2. 로그인
  - 로그인시 session 쿠키가 발급됩니다.

3. 게시글 생성
  - 더이상 게시글을 생성할때 게시글 비밀번호를 입력하지 않아도 됩니다.
  - 로그인, 인증이 완료된 사용자만 게시글 생성이 가능합니다.

4. 게시글 조회
  - 변경사항 없음.

5. 게시글 수정
  - 로그인, 인증이 완료된 사용자만 게시글 수정이 가능합니다.
  - 본인이 작성한 게시글만 수정이 가능합니다.

6. 게시글 삭제
  - 로그인, 인증이 완료된 사용자만 게시글 삭제가 가능합니다.
  - 본인이 작성한 게시글만 삭제가 가능합니다.

7. 댓글 생성
  - 더이상 댓글을 생성할때 댓글 비밀번호를 입력하지 않아도 됩니다.
  - 로그인, 인증이 완료된 사용자만 댓글 생성이 가능합니다.

8. 특정게시글의 댓글 조회
  - 변경사항 없음.

9. 댓글 수정
  - 로그인, 인증이 완료된 사용자만 댓글 수정이 가능합니다.
  - 본인이 작성한 댓글만 수정이 가능합니다.

10. 댓글 삭제
  - 로그인, 인증이 완료된 사용자만 댓글 삭제가 가능합니다.
  - 본인이 작성한 댓글만 삭제가 가능합니다.

***
## Level3_Express_jwtLogin

### Level3_Express_jwtLogin에서 변경된 내용은 다음과 같습니다.

1. 로그인 후 인증방식
- 위의 session id를 통해 인증하는방식에서 요청시 JWT를 통해 인증하는 방식으로 변경되었습니다.

***
## Level 4-5_express

### Level 4-5_express에서 변경된 내용은 다음과 같습니다.

1. 좋아요 기능 추가
- 로그인 한 유저가 게시글에 좋아요를 누르면 좋아요 수가 1만큼 올라갑니다.
- 이미 좋아요를 누른 게시글에 다시 좋아요를 누르면 좋아요 수가 1만큼 내려갑니다.
- 유저는 본인의 정보에서 좋아요를 누른 게시글을 확인할 수 있습니다.

2. CI/CD적용
  - Git Actions를 이용한 CI/CD

3. 로그인
  - 서버로 만료된 Access token이 들어오면 Refresh token검증을 통해 Access Token을 발급받습니다.
  - 구글 계정, 카카오 계정으로 로그인이 가능합니다.(개발 중)

4. 채팅기능
- 로그인 한 유저는 채팅방을 생성하고 채팅을 할 수 있습니다.

5. 회원가입
  - 회원가입 시 이메일 인증을 거쳐야합니다.(개발 중)

6. Dev / Prod 개발환경 분리
  - 개발서버 / 배포서버를 따로 두어 개발이 완료된 기능들만 배포서버로 옮길 예정.(개발 중)

7. Swagger API 작성 (개발 중)

***
## Level2_Nest.js

### 레벨2_Nest에서 변경된 내용은 다음과 같습니다.

1. 회원가입
  - nickname과 password로 회원가입이 가능합니다.

2. 로그인
  - 로그인시 jwt토큰이 발급됩니다.

3. 게시글 생성
  - 더이상 게시글을 생성할때 게시글 비밀번호를 입력하지 않아도 됩니다.
  - 로그인, 인증이 완료된 사용자만 게시글 생성이 가능합니다.

4. 게시글 조회
  - 변경사항 없음.

5. 게시글 수정
  - 로그인, 인증이 완료된 사용자만 게시글 수정이 가능합니다.
  - 본인이 작성한 게시글만 수정이 가능합니다.

6. 게시글 삭제
  - 로그인, 인증이 완료된 사용자만 게시글 삭제가 가능합니다.
  - 본인이 작성한 게시글만 삭제가 가능합니다.

7. 댓글 생성
  - 더이상 댓글을 생성할때 댓글 비밀번호를 입력하지 않아도 됩니다.
  - 로그인, 인증이 완료된 사용자만 댓글 생성이 가능합니다.

8. 특정게시글의 댓글 조회
  - 변경사항 없음.

9. 댓글 수정
  - 로그인, 인증이 완료된 사용자만 댓글 수정이 가능합니다.
  - 본인이 작성한 댓글만 수정이 가능합니다.

10. 댓글 삭제
  - 로그인, 인증이 완료된 사용자만 댓글 삭제가 가능합니다.
  - 본인이 작성한 댓글만 삭제가 가능합니다.

***
## Level3_Nest.js

### Level3_Nest에서 변경된 내용은 다음과 같습니다.

1. ODM을 사용했던 프로젝트를 ORM 프로젝트로 리팩토링 진행
  - Mongoose -> TypeORM

***

## Level 4-5_Nest.js

### Level 4-5_Nest.js에서 변경된 내용은 다음과 같습니다.
1. 좋아요 기능 추가
- 로그인 한 유저가 게시글에 좋아요를 누르면 좋아요 수가 1만큼 올라갑니다.
- 이미 좋아요를 누른 게시글에 다시 좋아요를 누르면 좋아요 수가 1만큼 내려갑니다.
- 유저는 본인의 정보에서 좋아요를 누른 게시글을 확인할 수 있습니다.

2. CI/CD적용
  - Git Actions를 이용한 CI/CD

3. 로그인
  - 서버로 만료된 Access token이 들어오면 Refresh token검증을 통해 Access Token을 발급받습니다.
  - 구글 계정, 카카오 계정으로 로그인이 가능합니다.(개발 중)

4. 회원가입
  - 회원가입 시 이메일 인증을 거쳐야합니다.(개발 중)

5. Dev / Prod 개발환경 분리
  - 개발서버 / 배포서버를 따로 두어 개발이 완료된 기능들만 배포서버로 옮길 예정.(개발 중)
