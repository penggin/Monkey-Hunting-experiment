# 물리 세특

# 소개

- 본 페이지는 **물리** 과목의 세특 제출을 위하여 제작되었습니다. (30714 이동훈)
- 프로그램을 잘 모르더라도 최대한 이해할 수 있도록 작성하였습니다.

# 탐구주제

물리엔진으로 실험해보는 원숭이사냥 이론

# 주제 선정 동기

예전에 수업시간에 이 이론을 직접 시행한 영상을 학교에서 봤을때, 저게 진짜로 된다고? 라는 생각과 함께 나도 한번 실험을 진행해보고 싶었는데, 이 실험을 내 희망진로이자 관심사인 **소프트웨어(코딩)** 을 통해서 진행해본다면 어떨까? 라는 생각이 들어서 이 주제를 선정하게 되었습니다.

# 교과서와 연관된 학습내용

물리2 교과서의 **1-1, 3. 등가속도 운동** 과 **1-1, 4. 포물선 운동** 단원을 참고하였습니다.

# 탐구방법

원숭이 샤냥 이론을 수식을 유도해보며 유도한 수식을 통해 반응적으로 그래프를 그려본 후, 게임엔진 중 하나인 “언리얼 엔진” 을 통해 직접 실험을 해볼 수 있는 프로그램을 제작 - 실험 해 볼 것입니다.

# 탐구 내용

---

## 게임엔진이 뭐야?

게임엔진이란, 게임을 만들기 위한 도구들을 모아 둔 엔진으로, 소리 연산등을 담당하는 사운드엔진, 물리 연산을 담당하는 물리엔진, 그래픽 연산을 담당하는 그래픽 엔진 등이 있다. 우리가 이번 탐구에서 사용할 엔진은 **유니티 엔진** 으로 게임제작 뿐만 아니라 영화, 건축물 시뮬레이션 등에서도 사용되는 다용도의 엔진이다.

## 먼저 원숭이 사냥 실험을 증명해보자!!

### 그래서 원숭이 사냥 실험이 뭔데?

우리 학교에서 물리수업을 들은 친구라면 알겠지만, 모르는 친구들이 더 많을것이다.

이 실험이 뭔지 모르는 친구를 위해, 한번 짚어보고 넘어가보자.

[https://youtu.be/0jGZnMf3rPo](https://youtu.be/0jGZnMf3rPo)

위의 영상처럼, 대포알의 초기발사방향이 원숭이를 겨냥하고 있다면, 속도와 관계없이 무조건 명중하게 된다는 내용의 실험이다.

(아직 잘 모르겠다면, 인터넷에 “물리 원숭이 사냥” 등으로 검색해서 더 알아보자.

### 등가속도 운동 공식

처음속도 $V_0$ 가속도 $a$ 를 가진 물체가 시간 $t$ 동안 등가속도 운동을 하여 나중속도가 $v$ 가 되었다면, 나중속도 $v$는 다음과 같이 나타낼 수 있다.

$$
v = v_0 + at
$$

이것을 그래프로 나타낸다면 아래의 그림과 같이 나타낼 수 있다.

![Untitled](https://user-images.githubusercontent.com/77449586/178145300-172287ad-41bc-408e-8c92-f286d7a11fa3.png)

이때, 일정한 가속도 $a$ 로 시간 $t$ 동안 운동한 물체의 변위 $s$ 는 **시간 - 속도 그래프** 에서 색칠한 부분의 넓이로 나타낼 수 있다.

$$
s=v_0t + \frac{1}{2}at^2
$$

속도 $v$ 를 구하는 식과 변위 $s$ 를 구하는 식으로부터 속도 $v$, 가속도 $a$, 변위 $s$ 의 관계를 구하면 다음과 같다.

$$
2as = v^2 - v^2_0
$$

### 준비는 모두 끝났다. 이제 본격적으로 증명해보자!

![Untitled 1](https://user-images.githubusercontent.com/77449586/178145319-883f1f9c-0a33-4307-b468-e9eb77812e05.png)


(그림판으로 그린 아주 멋진 그림이다.)

위의 그림에서,

- L = 대포와 원숭이와의 수평 거리
- H = 대포와 원숭이와의 수직 거리 (높이)
- $v_0$ = 대포알의 초기속도
- $\theta$ = $v_0$ 의 벡터와 밑변이 이루는 각
- O = 원점, x축과 y축의 교점

대포알은 지표면과 $\theta^\circ$를 이루며, $v_0$ 의 속도로 발사된다.

여기서, 수평으로의 속도는 다음과 같다.

$$
v_{수평} = v_0\cos\theta
$$

이때, 이동거리는 `속도 * 시간` 이므로 이동거리를 $s$로 나타낼 때,

$$
s_{수평}=v_0\cos\theta\times t
$$

이와 비슷하게 수직 이동속도를 구해본다면 다음과 같다.

$$
v_{수직}=v_0\sin\theta-\frac{1}{2}gt
$$

(이때, $-\frac{1}{2}gt$는 중력가속도로 인한 속도변화 이다.)

위를 바탕으로 이동거리를 구하면,

$$
s_{수직}=v_0\sin\theta\times t - \frac{1}{2}gt^2
$$

이제, 대포알의 x좌표(수평위치) 가 원숭이의 x좌표(수평위치) 와 일치하게 되는 시간을 구해보자.

$t$를 걸리는 시간이라고 설정하면 `거리 = 시간 * 속도` 에 의해서 아래의 식을 유도할 수 있다.

$$
t = \frac{L}{v_0\cos\theta}
$$

위의 과정을 통해 원숭이와 대포알의 x좌표(수평위치) 가 일치하게 되는 시간인 $t$를 알아냈다.

이제, t초뒤 원숭이와 대포알의 y좌표(높이) 까지 일치하게 된다는 것을 증명하면, 이 문제를 증명할 수 있다.

한번 증명해보자! 으쌰으쌰!!

먼저, $t$초 후의 대포알의 y좌표는 다음과 같이 유도할 수 있다.

$$
y_{대포알} = v_0\sin\theta\times t - \frac{1}{2}gt^2
$$

이때, 위에서 구한 $t$를 위의 식에 대입하면,

$$
y_{대포알} = (v_0\sin\theta)(\frac{L}{v_0\cos\theta})-\frac{1}{2}g(\frac{L}{v_0\cos\theta})^2
$$

위와 같은 방법으로 원숭이의 y좌표을 구하면,

$$
y_{원숭이}=H-\frac{1}{2}g(\frac{L}{v_0\cos\theta})^2
$$

이때, y좌표가 같아야 이 이론이 성립하므로 `대포알의 y좌표 = 원숭이의 y좌표` 의 형태로 식을 세우면

$$
(v_0\sin\theta)(\frac{L}{v_0\cos\theta}) - \frac{1}{2}g(\frac{L}{v_0\cos\theta})^2 = H - \frac{1}{2}g(\frac{L}{v_0\cos\theta})^2
$$

이때, 양변을 정리하면

$$
H=L\frac{\sin\theta}{\cos\theta}
$$

여기서 $\frac{\sin\theta}{\cos\theta}$=$\tan\theta$ 이므로, 위의 식에 대입하면,

$$
H = L\tan\theta
$$

이때, $\tan\theta$ = $\frac{H}{L}$이므로 위의 식에 대입하면 $H = H$ 로 등식이 성립함으로 이론을 증명할 수 있다.

## 유니티 엔진을 이용해 구현해보기

세상은 넓고, 사람은 많다.

분명 “나는 직접 실험 안해보고는 못믿어!!” 라는 사람도 한명쯤은 존재할것이다.

이런 사람들을 위해서 위에 있던 영상을 보여줄 수는 있지만, 극단적으로 먼 거리 (1km?) 에서는 성립하지 않는다고 반박할수도 있을것이다.

물론, 직접 실험을 해보는것을 통해서는 이런 극단적인 조건을 실험하지 못한다.

이런 상황을 위해서, 물리학자들은 극단적인 조건에서의 연구를 위해 때때로 **물리엔진** 을 이용한다.

우리도 한번 물리엔진을 통해 원숭이 실험을 구현해보도록 하자!

### 기획하기

우선, 무언가를 만들기 위해서는 **기획** 과정이 필요하다. 한번 우리가 만들 가상실험 프로그램을 기획 해보도록 하자.

- 기능
    - 대포알의 속도와 원숭이의 속도를 실시간으로 확인할 수 있는 GUI
    - 동시에 원숭이를 수직낙하시키며, 대포를 발사
    - 카메라
    - 카메라의 이동 (원숭이와 대포알의 거리, 위치에 맞추어 자동으로 이동함)
- 오브젝트(물체)
    - 대포
    - 대포알
    - 원숭이

## 코딩하기!

코딩하는 과정과 작성한 코드를 소개하는것은 아무래도 C#의 난이도가 조금 있다보니 누구나 이해할 수 있도록 작성하는것이 어려워서 생략하겠습니다.

**코딩중에 사용된 수학적 개념**

코딩하던 도중, 수학적 개념이 사용되어 이쪽내용을 한번 소개해보고자 한다.

이 프로그램에는 조절할 수 있는 인자가 3개 있는데, 그것은 **속도**, **(원숭이의)높이**, **(원숭이와 대포알의 초기위치 사이의) 거리** 이다.

하지만, 이 3가지중 속도는 벽면과 $\theta$도의 각도를 이루고있는 벡터의 크기인데, 프로그램의 구현 과정에서는 대포알의 수직속도와 수평속도가 필요했다.

하지만, 지금 우리의 프로그램에서는 바닥과 대포알의 벡터 사이의 각도가 제시되지 않고, 거리와 높이만이 제공되었다.

이때, 나는 각도를 얻기 위한 방법으로 **삼각함수** 를 사용하였다.

![Untitled 2](https://user-images.githubusercontent.com/77449586/178145313-ad884c1a-d5c9-4f55-a47b-89313da8c0dd.png)


우리가 미적분을 배우기 이전까지 다루는 삼각함수는 $\sin$,  $\cos$, $\tan$ 3가지가 있으며, 각각 `b/c`,

`a/c` , `b/a` 의 값을 가진다.

하지만, 지금 상황은 a 와 b 를 알고있으며, B의 각도를 모른다.

이때, 역함수의 개념을 사용하면 된다.

역함수란, 수학에서 정의역과 치역을 서로 뒤바꾸어 얻는 함수로, 이전의 입력값이 출력값, 이전의 출력값이 입력값의 형태로 나오는 함수이다.

그렇다면 우리는 이제 탄젠트의 역함수에 높이/밑변 값을 넣으면 각도를 알 수 있다는것을 알게되었다.

이를 수식으로 구현해보자면 다음과 같다.

$$
\tan^{-1}(\frac{b}{a})
$$

이 각도를 위쪽에서 유도한 공식에 대입하면, 수평방향속도, 수직방향속도를 구할 수 있다!

이를 C# 코드로 구현하면 다음과 같다.

```csharp
using static System.Math;

double xSpeed = Speed * Cos(Atan(b/a));
double ySpeed = Speed * Sin(Atan(b/a));
```

위에서는 탄젠트를 직접 역수로 만드는 대신, Atan() 이라는 함수를 사용하였는데, 사실 탄젠트의 역함수인 코탄젠트(cot) 는 공학분야에서 아크탄젠트(arctan) 이라고 불린다.

소요시간 : 약 4시간

사용 IDE : Visual Studio Code

코드 : https://github.com/penggin/Monkey-Hunting-experiment

**작동 모습**

![asdf6](https://user-images.githubusercontent.com/77449586/178145331-1f057f4f-5138-492c-80cb-3a036c2c2ca5.gif)

거리 최대, 속도 30일때

![asdf7](https://user-images.githubusercontent.com/77449586/178145335-4c4ea39d-eb43-40c8-a3ac-581f5a4522ff.gif)

거리 최대, 속도 70일때

# 느낀점

나의 진로이자 취미인 코딩을 통해 수업시간에 배웠던 내용을 직접 탐구해보고 구현해 보아서 매우 뜻깊은 활동이었다.

이 프로젝트를 진행하면서 이전에는 사용해보지 않은 C#이라는 언어를 새로 사용해 보았으며, 처음 문법을 익힐때와 유니티 엔진의 사용법을 배울때는 조금 힘들었지만, 조금 익숙해지고 나니 수월하게 진행할 수 있었다.

원래는 속도, 각도, 거리 3가지를 조절할 수 있도록 만들려고 했지만, 생각보다 구현이 까다로워서 높이로 바꾸었는데, 나중에 시간이 생기면 이것을 더 고퀄리티로 구현해보며 바꾸어봐야겠다.

이 활동을 진행하면서 물리 과목에 조금 더 흥미가 생겼으며, 소프트웨어 개발자라는 나의 꿈에 한발자국 더 나아갈 수 있게 되어서 의미있었고, 나중에도 이런 프로젝트를 더 진행해보고 싶다는 생각이 들었다.

# 정리 (세특에 쓰이기 원하는 내용?)

“물리” 수업시간에 다룬 내용인 “원숭이 사냥 실험” 을 수학적 관점에서 탐구하고, 이를 프로그램으로 구현하는 과정을 보고서로 작성함.

평소 소프트웨어 개발자를 희망하는 학생으로 자신의 관심분야인 “소프트웨어” 와 학교 수업시간에 다룬 내용을 융합시켜서 탐구해보는 활동을 통해 물리 개념을 조금 더 잘 이해할 수 있게 되었으며, 처음 다루는 도구인 유니티와 C#에도 익숙해질 수 있는 기회였다고 말함.

# 긴 글 읽으시느라 수고하셨습니다!!
