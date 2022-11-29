<hr> <!-- Header -->
<div align="center" style="font-weight: bold; font-size: 36px;">
    <span class="Docs" style="color: gray; background-color: rgb(50, 209, 248); border-radius: 0.4rem;"><span style="margin: 0.3rem;">Docs</span></span>
    <span>대입연산자 vs 복사생성자</span>
</div>
<div align="right" style="color: gray;">
    <span>Create </span><span>2022.11.15.</span>
    <span style="margin: 4px; font-weight: bold; font-size: 20px;">·</span>
    <span>Edit </span><span>2022.11.29.</span>
</div>
<hr>
<br>
<br>

```cpp
#include <iostream>
using namespace std;

int main(int argc, char* argv[])
{
    Point pos1(0, 0);
    Point pos2(1, 0);
    pos2 = pos1;  // pos2.operator=(pos1);
    // 대입 연산자가 호출된다
}
```

```cpp
#include <iostream>
using namespace std;

int main(int argc, char* argv[])
{
    Point pos1(0, 0);
    Point pos2 = pos1;  
    // 복사 연산자가 호출된다
}
```
