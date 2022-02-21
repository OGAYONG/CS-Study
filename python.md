# Python 

### 파이썬 vs 아나콘다

#### 파이썬

-  패키지 관리 시스템인 pip만 포함함 - 필요할 때마다 직접 설치
- 파이썬은 컴퓨터 자체 환경에 패키지나 툴이 설치되어, 프로젝트를 여러개 진행 시 불필요한 패키지들이 포함되어 공간 차지함



#### 아나콘다

- pandas, numpy, scipy 등 여러 패키지들이 포함되어 있음

- 분리된 가상환경으로, 프로젝트마다 필요한 패키지들을 설치해 관리 가능함
- 논리적으로 다른 환경이 되어버림



### list vs tuple

``` python
>>> my_list = [1,2,3]
>>> my_tuple = (1,2,3)
>>> my_list[1] = "two"
>>> my_list
[1, 'two', 3]
>>> my_tuple[1] = "two"
Traceback (most recent call last) :
    File"<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment

```

- List는 가변적이지만, tuple은 불변적이다.
- tuple은 **append**로 새로운 요소를 추가할 수도 없음.
- 따라서 list는 단일 종류의 요소를 갖고 있고, 그 일련의 요소가 몇개나 들어있는지 명확하지 않은 경우에 주로 사용
- 