# Подключение библиотеки в Python
Для работы в Python нужно подключить пакет numpy:
```Python
import numpy as np  
```

# Сумма
$$\sum_{k=-2}^3 (2k+k^2)$$
```Octave
s = 0
for k = -2:3
  s = s + (2*k + k^2)
endfor
```

```python
s = 0  
for k in range(-2, 4):  
    s += 2*k + k**2  
print(s)
```

# Матрицы
## Задать матрицу
$$A = \begin{bmatrix}
4 & 2 & 1 \\
2 & 2 & 1 \\
1 & 1 & 1
\end{bmatrix}$$
```python
A = np.array([[4, 2, 1],  
              [2, 2, 1],  
              [1, 1, 1]])
```

```Octave
A = [4 2 1; 2 2 1; 1 1 1]
```

## Операции с матрицами

```Python
A + B # Сложение матриц
A - B # Вычитание матриц
A * 3 # Умножение матрицы на число
A @ B # Умножение матриц
np.linalg.det(A) # Определитель матрицы
np.linalg.inv(A) # Обатная матица
A.T # Транспонированная матрица
```

```Octave
A + B % Сложение матриц
A - B % Вычитание матриц
A * 3 % Умножение матрицы на число
A @ B % Умножение матриц
det(A) % Определитель матрицы
inv(A) % Обратная матрица

% Транспонирование матрицы:
A.' 
A'
transpose(A)
```
	
```Python
try:  
    inv_matrix = np.linalg.inv(A)  
    print(inv_matrix)  
except np.linalg.LinAlgError as err:  
    if 'Singular matrix' in str(err):  
        print('Определитель не существует', err)  
    else:  
        print(err)  
```
