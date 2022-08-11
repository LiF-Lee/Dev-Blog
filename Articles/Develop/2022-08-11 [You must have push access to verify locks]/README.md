# You must have push access to verify locks

**`📌 Create`** `2022-08-11`

**`🖍 Edit`** `2022-08-12`

<hr>

git lfs 용량 생각을 안하고 작업해서,
프로젝트 한 개 만으로 lfs 무료 용량이 가득 찼다 ㅡㅡ

어쩔 수 없이 프로젝트 삭제하고 재생성해서 작업하는 중에 아래와 같은 메세지와 함께 push가 갑자기 안되는 경우가 생겼다.

```bash
error: Authentication error: Authentication required: You must have push access to verify locks
error: failed to push some refs to 'https://github.com/LiF-Lee/Project-A.git'
```

검색 해보니 lfs에서 deploy 된 키로 인증이 안되는 문제라고 한다.

아래와 같이 입력해서 해결했다.

```bash
$ git lfs locks
$ git config 'lfs.locksverify' false
```