# 7주차/과제

## P3.1

---

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ad9fdd74-3741-4993-828d-2b3b572a4652/a1a6420e-b52e-46e4-a963-1b42b3d59859/Untitled.png)
```matlab
syms s k M b

A = [0,1;-k/M,-b/M]
B = [0;1/M]
C = [1,0];
D = 0;

Phi = inv(s*eye(2)-A);

G = C * Phi * B + D;

pretty (G)
```

## P3.3

---

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ad9fdd74-3741-4993-828d-2b3b572a4652/5e4f7b8a-e273-4896-a342-1714ffdca499/Untitled.png)
## P3.5

---

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ad9fdd74-3741-4993-828d-2b3b572a4652/ebc13504-53a4-42e5-98f1-4f5cc0f25292/Untitled.png)
```matlab
clear 
clc;

syms s 

Ts = (s+2)/(s^3+5*s^2-23*s+2)

[num,den]=numden(Ts)
n=sym2poly(num)
d = sym2poly(den)
[A,B,C,D] = tf2ss(n,d)

Phi = inv(s*eye(3)-A)
G = C * Phi * B + D
```

## P3.17

---
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ad9fdd74-3741-4993-828d-2b3b572a4652/a146176c-d428-450e-b3a4-e39d8e61ff37/Untitled.png)
손으로 문제 푸는 것이 불가능하기 때문에 매트랩 코드 이용

```matlab
clc
clear

syms s

A = [1 1 -1;4 3 0;-2 1 10]
B = [0;0;4];
C = [1 0 0];
D = 0;
Phi = inv(s*eye(3)-A);
G = C * Phi * B + D
```

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ad9fdd74-3741-4993-828d-2b3b572a4652/413fc6d7-b185-4253-b3f4-c5eaadb895e4/Untitled.png)
