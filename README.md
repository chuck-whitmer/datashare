# datashare
This repo contains the data necessary to reproduce the CRAM calculations for the Whitmer and Zimmerman
article "Computing the Time-Averaged Nuclide Inventory Using the Chebyshev Rational Approximation Method".
Typically the construction of a transmutation matrix M will be complex and require many assumptions. 
By providing the exact matrices used, we can avoid ambiguity.

## The list of nuclides
There are 3793 nuclides in the problem (regardless of whether they are used), and they are listed in 
the file `nuclidelist`, which begins with:
```
#   1:   10010  H   1
#   2:   20010  H   2
#   3:   30010  H   3
#   4:   30020  He  3
#   5:   40020  He  4
#   6:   50020  He  5
#   7:   50030  Li  5
#   8:   60020  He  6
#   9:   60030  Li  6
#  10:   60040  Be  6
[...]
```

A 4-digit id number is provided in text columns 2 through 5. There follows an `'AZS'` identifier, 
which provides 3 digits of the mass number A followed by 3 digits for the atomic number Z. 
A last digit S indicates any metastate level. 
Three more fields help with human interpretation of the nuclide.

These two entries show familiar examples:
```
#3418: 2350920  U 235
#3419: 2350921  U 235*
```
The rows of each matrix correspond in order to the production of the listed nuclides. Thus the first row of the 
matrix details H1 productions, etc.

## The decay matrix for 


```
 3793  3793 134933
    1    7  2.25876488597760e+21
    1   10  2.79872884969594e+20
    1   20  8.21371482728727e+17
    1   21  3.37532540098756e+00
    1   37  8.07863846806463e+01
    1   49  6.08397419959576e+19
    1   54  6.34750165347935e+00
    1   65  1.73286795139986e+07
[...]
    3    3  xxxxxxxxxxxxxxxxx	
```

	
![neutron spectrum](BurnSpectrum.png "a title")	
