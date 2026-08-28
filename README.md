# ECE-2112-PA-1
Made by Marcus Nathan J. Calpe | 2ECE-D

This repository contains the source code for ECE2112 Practical Activity 2 (AY 2026–2027) with solutions to three Python programming problems.

### A. Reproducible Normalization Problem: Create a reproducible random 5 × 5 integer ``ndarray`` named X. Use the following two statements before performing any calculation:

```python
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))
```
As per the requirement, this parameter was set to eliminate the need of creating a new set of array with a size of 5x5 from 10 - 100, excluding 101.
```python
mean = X.mean()
std = X.std()
```
This section defines mean and std of the array. Using the ``X.mean()`` calculates the arithmetic average of the given array, the same goes with ``X.std()``, which calculates the standard deviation of the given array.
```python
X_normalized = (X - mean) / std
```
Using this applies the standard score formula to every element of the matrix.
```python
normalized_mean = X_normalized.mean()
normalized_std = X_normalized.std()
```
This re-calculates the average of the new data of mean and standard deviation. The mean should output a 0 and the standard deviation should output 1.

### B. Cubes Divisible by 4:Using NumPy, create the first 100 positive integers, cube every element, and reshape the result into a 10 × 10 ndarray named C. Thus, C begins with 13 and ends with 1003. Use a Boolean condition on C to obtain every cubed value divisible by 4. Store the selected values in div by 4. Preserve NumPy’s normal row-major selection order.

```python
C = (np.arange(1,101)**3).reshape(10,10)
```
The ``np.arange(1,101)`` creates an array of the first 100 positive integers, alongside this, the ``**3`` operator cubes every element of the array. Finally, ```.reshape(10,10)``` restructures the result into a 10x10 matrix.
```python
div_by_4 = C[C % 4 == 0]
```
Finally, the line above applies a Boolean condition to filter the matrix wherein for every element in C, when divided by 4 (``C[C % 4]``), it should equal to 0 (``C[C % 4 ==0``).

### C. Above-Mean Squares Problem: Create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing row-major order. Compute the mean of all elements of S and store it in S mean. Then use Boolean filtering to select only the elements strictly greater than S mean. Store these values in above mean.

```python
S = (np.arange(1,37)**2)
```
``np.arange(1,37)`` was used to create to create an array containing 1 up to 36, excluding 37, storing them in `S`. And `**2` operator was used to square the array.

```python
S_mean = S.mean()
```
`S.mean()` calculates the mean of the squared values of the array. After this, it was stored in the `S_mean` variable.

```python
above_mean = S[S > S_mean]
```
Lastly, this Boolean filtering was used to filter the array, extracting only the squared values that are strictly greater than the calculated mean `S_mean` and storing them in the `above_mean` variable.


Thank you for reading!

To see the main Python program for Programming Assignment 2, click this link: [https://github.com/MarcusCalpe/Python-Assignment-2/blob/main/Python%20Assignment%202.ipynb](https://github.com/MarcusCalpe/Python-Assignment-1/blob/main/Python%20Assignment.ipynb) and download it, open it in Jupyter Notebook, then run all cells.

#### README file Version History:
August 27, 2026 - Initial README output created.

August 28, 2026 - Uploaded Python Assignment 2 and required .npy files.

August 28, 2026 - Updated README file.
