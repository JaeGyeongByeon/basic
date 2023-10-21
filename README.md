# 7주차/과제

## P3.1

---
![Untitled 1](https://github.com/JaeGyeongByeon/basic/assets/144103220/0af25824-3ffe-411f-b092-3591936c7dd0)


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

![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/27fc3787-9851-4bc2-a529-2bc553483de8)

## P3.5

---

![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/4a05a84d-955d-4bfe-badb-3050ee1f3832)

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
![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/c893cf61-3a6e-4b88-bf06-91d70a5fa1c2)

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

![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/eb3c8e9f-896e-4fff-b50e-9da58738c34d)
