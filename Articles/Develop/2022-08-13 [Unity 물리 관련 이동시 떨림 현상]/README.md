<hr> <!-- Header -->
<div align="center" style="font-weight: bold; font-size: 36px;">
    <span class="Error" style="color: gray; background-color: rgb(254 205 211); border-radius: 0.4rem;"><span style="margin: 0.3rem;">Error</span></span>
    <span>Unity 물리 관련 이동시 떨림 현상</span>
</div>
<div align="right" style="color: gray;">
    <span>Create </span><span>2022.08.13.</span>
    <span style="margin: 4px; font-weight: bold; font-size: 20px;">·</span>
    <span>Edit </span><span>2022.08.13.</span>
</div>
<hr>
<br>
<br>

기존에 작성했던 코드에서 여러가지 수정해야 해결될 줄 알았는데

```cs
void Update()
{
    // 물리 관련 이동을 처리하는 코드
}
```

물리 관련 이동 코드를 `Update`에서 처리해서 발생한 문제라고 한다.

그래서 아래와 같이 `FixedUpdate`에서 처리하니 떨림 문제가 해결되었다.

```cs
void FixedUpdate()
{
    // 물리 관련 이동을 처리하는 코드
}
```