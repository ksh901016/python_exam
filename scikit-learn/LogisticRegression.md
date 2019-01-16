**정규방정식(normal equation)에 대해 알아보기** (http://daeson.tistory.com/172)



### Logistic Regression

분류(classification) 알고리즘

=> 이진 분류 : Binary Classification 의 예 (양성, 음성)

regression으로 분류는 어렵지 않은가..? (크나큰 오류가 존재하기 때문에)

> sigmoid = logistic function이 존재함
>
> **linear 함수를를 logisitic 함수로 매핑 시킨다.**
>
> linear 함수를 logistic(=sigmoid) 함수로 치환하여 사용

![logisticRegression](image/logisticRegression.jpg)

Logistic Regression 이란 말이 있지만, 회귀가 아닌 분류(Classification)이다.



**Decision Boundary(결정경계)**

> sigmoid function을 활용하면 positive(z >=0)와 negative(z < 0)의 구분이 매우 확연하다.



**Logistic Regression**

z >= 0 , g(z) >= 0.5 

>  y = 1,  악성

z < 0 , g(z) < 0.5 

> y = 0, 양성

두개의 비용함수(cost function)를 가진다. (y=0, y=1 일때) 

두개를 합쳐서 한 식으로 표현할 수 있음

j(g(z), y) = -ylog(g(z))  - (1-y)log(1-g(z))



### Support Vector Machines

![SupportVectorMachines](image/svm.jpg)



---------------------

### 광섭 상무님 발표

지난번에 보내주신 것에 대한 설명

1. 파이썬 기초
2. Scikit-learn
3. Scikit-learn, Tensorflow(핸즈온_머신러닝)



### Logistic Regression



**Machine Learning 기초** (scikit-learn)

데이터 -> feature, label 

데이터를 가장 잘표현할 수 있는 모델을 만들어서, 새로운 input이 들어왔을 때 예측을 잘 할 수 있도록하는 것이 목적. (적절한 파라미터를 찾는 것)

맥락은 똑같음 (Logisitic Regression 포함)



Linear 가지고는 classification이 불가능 하기 때문에, Logistic Function(Sigmoid 함수)이 나옴. 

Logisitic Function은 0~1 사이로 모든 값을 가둠(확률을 나타내기에 유리함)

최적화하면서 라인을 잡아가는 과정

Logistic Function만 가지고는 에러를 찾기가 힘듬 (Cost Function을 구하기가 직관적이지 않음)

input 데이터(치환된 값, z)를 가지고 확률적으로 가장 높은 파라미터를 찾는 것

가늠도..? 

P(악성|X) (likelihood)   ... maximum likelihood..?

=> 이항분포의 누적확률 분포가 Sigmoid 함수

