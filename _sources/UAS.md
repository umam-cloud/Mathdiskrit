---
title: UAS

---

# UAS

## 1
| P   | Q   | R   | S   | $(P \rightarrow Q)$ | $(R \rightarrow S)$ | $(P \rightarrow Q)\rightarrow(R \rightarrow S)$ |
| --- | --- | --- | --- |:-------------------:|:-------------------:|:-----------------------------------------------:|
| T   | F   | T   | T   |          F          |          T          |                        T                        |
| T   | T   | F   | T   |          T          |          T          |                        T                        |
| F   | F   | T   | F   |          T          |          F          |                        F                        |
| F   | T   | T   | F   |          T          |          F          |                        F                        |
| T   | F   | F   | F   |          F          |          T          |                        T                        |
| F   | T   | T   | F   |          T          |          F          |                        F                        |
| T   | F   | F   | T   |          F          |          T          |                        T                        |
| F   | T   | T   | T   |          T          |          T          |                        T                        |


## 2

![downloadg](https://hackmd.io/_uploads/HJB7pMENyx.png)


| Node | a   | b   | c   | d   | e   | f   | g   |
|:----:| --- | --- | --- | --- | --- | --- | --- |
|  a   |  0  |  1  |  2  |  3  |  1  |  2  |  3  |
|  b   |  1  |  0  |  1  |  2  |  2  |  1  |  2  |
|  c   |  2  |  1  |  0  |  1  |  3  |  1  |  2  |
|  d   |  3  |  2  |  1  |  0  |  4  |  2  |  1  |
|  e   |  1  |  2  |  3  |  4  |  0  |  3  |  4  |
|  f   |  2  |  1  |  1  |  2  |  3  |  0  |  1  |
|  g   |  3  |  2  |  2  |  1  |  4  |  1  |  0  |


### Menghitung Closeness Centrality

$Cc(b): (\frac{7-1}{1+1+2+2+1+2})=(\frac{6}{9})=0,666666667$