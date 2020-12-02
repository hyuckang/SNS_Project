## Users

```
class User
    user_id -> PK
    user_name
    password
    email_add
    profile_url(프로필 사진 url)
```

- 유저 등록
  - Method : POST
  - URI : ~~/api/users/register~~
- 유저 정보 조회
  - Method : GET
  - URI : /api/users/{user_name}
- 유저가 등록한 posts 조회
  - Method : GET
  - URI : /api/users/{user_name}/posts
- 유저 삭제
  - Method : Delete
  - URI : /api/users/{user_name}
- 유저 정보 업데이트
  - Method : PUT
  - URI : /api/user/{user_name}



## Posts(게시물)

```
class Article
    posts_id -> PK
    user_id(업로드 한 user)
    content(게시물 내용)
    pic_url(게시물 사진 url)
    created_at
    updated_at
    tags(해시태그)
```

- 게시물 등록
  - Method : POST
  - URI : ~~/api/posts~~
- 모든 게시물 조회
  - Method : GET
  - URI : /api/posts
- 특정 게시물 조회
  - Method : GET
  - URI : /api/posts/{posts_id}
- 특정 게시물 업데이트
  - Method : PUT
  - URI : /api/posts/{posts_id}
- 특정 게시물 삭제
  - Method : Delete
  - URI : /api/posts/{posts_id}



## Comment(게시물 댓글)

```
class comment
    comment_id -> PK
    article_id
    user_id
    comment_content
```

- 특정 게시물의 댓글 조회
  - Method : GET
  - URI : /api/posts/{posts_id}/comment
- 특정 게시물에 댓글 달기
  - Method : POST
  - URI : /api/posts/{posts_id}/comment



## Likes





## Messages

```
class Messages
    msg_id -> PK
    sender_uid
    reciver_uid
    created_at
    updated_at
```





## Chats







