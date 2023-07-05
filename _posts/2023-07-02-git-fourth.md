---
layout: single
title:  "[Git]초심자의모험(diff,difftool -1/2)-Part3"
categories:
    - git
tag: [git,diff,difftool,문제,해결]
---

<code>commit</code>까지 해보았다.
{: .notice--info}

> <code>commit</code>전에 수정한 현재파일(staging안한 파일) 과 최근에 <code>commit</code> 한 파일의 차이점을 알고 싶지 않은가?

그래서 나온 git 문법 두둥

```terminal
git diff
```

수정한 파일과 '반드시', commit한 파일의 차이를 비교한다음,
<BR>
수정 파일을 staging한 후에 commit 하자 :fire:
{: .notice--info}

![git_sample](/assets/images/git/230701_git_10.PNG)

git diff 를 하면 ++ 된것이 추가 된 사항이라는 뜻이다.


commit한 모든 것과 차이를 볼 필요가 없지 않은가?
그래서 
이렇게 따라하자

```terminal
git diff 커밋한id

$ commit 한 것을 보려면 

git log --all --oneline으로 입력하고 노란색으로 -visual studio 기준- 
나오는 숫자+영문 조합이 있다. 
그것이 커밋한 id 
```
커밋한id와 지금 수정한 -add 안한- 파일과의 비교가 가능하다.

아니면
```terminal
git diff 커밋-1 커밋-2
```
과거의 특정 커밋 두 개간의 비교도 가능하다.

그런데 말입니다. :raised_eyebrow:
{: .notice--warning}

terminal 안에서만 차이를 보기가 너무 힘이듭니다.
<BR>
그래서,

```terminal
git difftool  terminal 안에서 입력해보자
```
![git_sample](/assets/images/git/230701_git_11.PNG)

y 입력 후 enter 그러면 vim terminal이라고 하는 것이 terminal 안에 띄워진다.

![git_sample](/assets/images/git/230701_git_12.PNG)

<div class="notice--info">

<ul>
<li>
방향키는 h,hj,k,l이라고 블로그나 강의에 나와있는데 화살키로도 된다. (한글로 되어있으면 방향키 안먹음)
</li>
<li>
종료하고 싶으면 커서 상관없이 <code>:</code>를 치면 맨 아래 <code>:</code> 나오고 qa 입력하면 탈출한다.
</li>
</ul>
</div>

> 그런데 여기서 내가 탈출 하려고 했는데 :가 맨 아래에 안뜬다. 
j,k,l,h 방향키로 이동하려고 해도 안되고 문자가 입력된다..;;

![git_sample](/assets/images/git/230701_git_14.PNG)

'vim terminal' 여기서 문자를 칠 수 있더라.
<BR>
문자치고 싶으면 사진에 내가 써 놓았다.
{: .notice--info}


## 문제의 시작

<div class="notice--info">
 <h3>이제 vim terminal에서 놀았으니  빠져나가 보자</h3>
 빠져나가는 방법은 내가 이것저것 해보니 --INSERT--를 없애야 한다.
<ul>
<li>
ESC키를 누르자-> 누르면 <code>--INSERT--</code>가 사라진다. 
</li>
<li>
사라진 상태에서 <code>:</code>을 누르면 vim화면 바깥으로 나가게 되는데 여기서 qa를 치면 탈출이다.
</li>
</ul>
</div>

![git_sample](/assets/images/git/230701_git_13.PNG)

```
빨간색으로 나를 위협한다. 
탈출이 불가능하다..
```

## 구글링으로 해결하기

> 구글링을 하다 보니 vim 에디터 종료 명령어가 나열되어있다. 

<div class="notice--info">
 <h3>VIM 에디터 종료 명령어(feat: <span style='color: red;'>E37: No write since last change (add ! to override))</span></h3>
 에디터 종료는 ESC 한 번 누른 후 :qa or :q인데 
 <BR>
 <span style='color: black;'>E37: No write since last change (add ! to override)</span> 이런 문구가 뜬다면 아래 2가지가 있다.
<ul>
<li>
<code>:wq</code>는 파일 저장 후 종료 명령어
</li>
<li>
파일 저장 하지 않고, 그냥 종료 명령어는<code>:q!</code>하면 저장하지 않고 종료
</li>
</ul>
</div>

나는 입력했으니 후자를 선택해 종료하겠다.!!

<code>:q!</code> 입력하면

![git_sample](/assets/images/git/230701_git_15.PNG)

이런 창이 한번 더 나오는데 
이 때는 <code>:qa</code> 를 입력하자

![git_sample](/assets/images/git/230701_git_16.PNG)

입력 후 엔터키 누르면 탈출 성공!

![git_sample](/assets/images/git/230701_git_17.PNG)


글이 너무 길어지니 다음에서 끝내겠다.
{: .notice--info}