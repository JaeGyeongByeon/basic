![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/76838b46-8ee3-424a-a2d1-61f07ac33ffe)
![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/d90f3a74-d824-43bc-8f36-1fc82c9f1b5d)
![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/fe6aa733-6eab-4a6a-83ac-d786410eb454)
![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/0deb1a1d-8ad3-4f57-a2e1-bde0b57bb930)
![image](https://github.com/JaeGyeongByeon/basic/assets/144103220/45c9f1a7-58e8-4a45-b5fc-50188a301fcd)
---
%1항
[M,L] = routh_hurwitz([1 5 2]);

모든 계수가 양수이므로 안정한 시스템
%2항
[M,L] = routh_hurwitz([1 4 8 4]);
모든 계수가 양수이므로 안정
[M,L] = routh_hurwitz([1 2 -6 20]);

a_1이 음수이므로 불안정

[M,L] = routh_hurwitz([1 1 2 12 10]);

음수 항이 존재하므로 불안정
syms K
[M,L] = routh_hurwitz([1 1 3 2 K]);
 k>0 이고, 2-k>0이어야한다.
그러므로 k의 범위는 0<k<2이다. 
[M,L] = routh_hurwitz([1 1 2 0 1 6]);

음수가 존재하므로 불안정
[M,L] = routh_hurwitz([1 1 2 1 1 K]);
불안정
