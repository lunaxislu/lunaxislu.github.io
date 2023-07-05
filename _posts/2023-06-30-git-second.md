---
layout: single
title:  "[Git]초심자의모험-Part1"
categories:
    - git
tag: [git,git-user,git-email]
---

들어가기에 앞서, 무섭다.
<BR>
<BR>
그러나 명령어(module)들을 배우고 문제를 해결해보며 큰 틀까지 이해하게 되기를, 그리고 <strong style="border-bottom:2px solid black; padding:0 4px 4px 4px">능숙하게 사용하는 날</strong>이 오기를..
{: .notice--info}

<div class='notice'>
    <h4>준비물</h4>
    <ul>
        <li>git install !! </li>
        <li>visual studio code install !!</li>
        <li>작업물 폴더 있어야함</li>
    </ul>
</div>

![git_folder](/assets/images/git/230630_git_01.PNG)

작업폴더에

shif+우클릭하면 powershell열기
<BR>
powershell말고 윈도우+R키 눌러 cmd켜서 해도 상관 읎다.

![git_version](/assets/images/git/230630_git_02.PNG)

git --version 이라고 입력 후
git version 어쩌구가 뜨면 git 설치 완성.

```
git config --global user.email "My-email@naver.com"
git config --global user.name "My-name"
```
그 다음 git에다 이메일과 이름을 등록해줄 텐데 
git version 확인 후 바로 위 코드와 같이 써도 무관하다.

난 처음에, 어디에다가 이메일과 이름을 써야하는지도 있을 거 같아서 찾아 봤는데 그런거 없다 전역으로 등록 하는 것이므로 저걸 터미널에서 등록만 해주면 된다.
{: .notice}

:question:여기서 의문은 왜 이메일과 이름을 등록하냐는 것이다.
<BR>
지금 이 posting은 git을 막 시작한 후 작성 하는 글이 아니고 git을 사용해보면서 git 연결을 어떻게 끊는지에 관해 구글링 하다가 git으로 연결끊고 다시 연결하는 방법의 글을 보았는데 
<BR>
<BR>
<span style="padding-bottom: 10px; display:block;">git을 통해 github에 commit을 하는 과정에서</span>
github에 일명 잔디심기라고 commit하면 초록색으로 색칠 되는 작업이 되려면 github의 이메일과 이름이 git의 이름과 이메일이 동일해야 commit이 잘 작동 된다고 한다.
{: .notice--info}

이메일과 이름이 잘 등록 되어있는지 확인 하고 싶으면
```
git config --global user.name
git config --global user.email
```
위의 명령어를 통해 확인 할 수 있다.

> config가 무엇인지 나와같이 궁금할 수 있으므로 
사이트 추천 들어간다. <BR>
[config에 관하여](https://www.daleseo.com/git-config/)


마치면서 <BR>
정보가 잘못 되면 **수정과 피드백 좋아요**
{: .notice--warning}

