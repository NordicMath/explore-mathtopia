# Linear algebra


## References


A top reference is the GTM volume by Roman (3rd edition).

Other good references:
- Axler
- Lax


A list of references:
https://begriffs.com/posts/2016-07-24-best-linear-algebra-books.html


## Preliminary notes for organisation

Ambition: Treat types of matrices over general rings, but treat categories of modules only over fields. The general theory of modules over a ring which is not a field will come later, in a different part of the Realm.

Types:
- R-matrix (for R a unital commutative ring).
- k-matrix (for k a field)
- Integer matrix
- Real matrix
- Complex matrix
- Matrix (means any of the above five)

Note: We could also talk about F-matrix and K-matrix, adopting the convention that F is a general field, while K is a characteristic zero field. Could also use a similar convention for algebraically closed fields... let's discuss this.

Categories:
- Euc_k
- Vec_k


## Zophie file on matrices

Type: Matrix

Representations:
- As a list of rows, each row itself a list.
- As a list of columns, each column itself a list.
- As a pair (n, L), where n is a positive integer (the length of a row) and L is the list of entries, read row by row.

Properties:
- Invertible
- Square

Invariants:
- Number of columns
- Number of rows
- Determinant
- Trace
- Characteristic polynomial

Unary operations:
- n-th power (for n a positive integer)
- Transpose

Binary operations:
- Addition
- Multiplication
- Kronecker product

Examples:
- The zero matrix of size m x n (for any positive integers m, n)
- The identity matrix of size n (for any positive integer n)
- The empty matrix

Other machines:
- The incidence matrix of a graph

Theorems:
- The identity matrix is invertible (stupid example!)

Algorithms:
- Input: A square matrix M. Output: Tr(M). Step 1: Sum the diagonal elements.




### Scattered notes for later versions

Type: R-matrix

Properties:
- Diagonalizable


Type: k-matrix  

- The matrix associated to a linear map between two vector spaces with chosen bases
