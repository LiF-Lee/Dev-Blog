<hr> <!-- Header -->
<div align="center" style="font-weight: bold; font-size: 36px;">
    <span class="Error" style="color: gray; background-color: rgb(254 205 211); border-radius: 0.4rem;"><span style="margin: 0.3rem;">Error</span></span>
    <span>You must have push access to verify locks</span>
</div>
<div align="right" style="color: gray;">
    <span>Create </span><span>2022.08.11.</span>
    <span style="margin: 4px; font-weight: bold; font-size: 20px;">·</span>
    <span>Edit </span><span>2022.08.12.</span>
</div>
<hr>
<br>
<br>

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