# Python

## copy 모듈_얕은 복사, 깊은 복사



**주소** : 모든 변수는 저장된 메모리 어드레스를 가지며, 각 개체는 고유의 주소가 있다.

**복사** : 변수의 주소를 공유하거나 다른 이름으로 저장해 사용하는 것이다.



|         얕은 복사          |             깊은 복사              |
| :------------------------: | :--------------------------------: |
|           copy()           |             deepcopy()             |
| 원본이 바뀌면 같이 바뀐다. | 원복이 바뀌어도 복사본은 안바뀐다. |

 

``` python
from copy import copy
from copy import deepcopy

a= [1,2,3]
b=a
c=deepcopy(a)
print("a 값 : {}".format(a))
print("b = a 값 : {}".format(b))
print("a 딥카피 값 : {}".format(c))
print("a 주소:{} b 주소:{}".format(id(a),id(b)))
print("a값을 1,2 세트 값으로 변경")

#수정을 할때
a.append(4)
print("a 값 : {}".format(a))
print("b = a 값 : {}".format(b))
print("a 딥카피 값 : {}".format(c))
print("a 주소:{} b 주소:{}".format(id(a),id(b)))

#a에 새로운 변수를 집어 넣으면 주소가 변경된다.
a= [1,2]
print("a 값 : {}".format(a))
print("b = a 값 : {}".format(b))
print("a 딥카피 값 : {}".format(c))
print("a 주소:{} b 주소:{}".format(id(a),id(b)))
```

