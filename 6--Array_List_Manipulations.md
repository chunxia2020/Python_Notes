## Create and Get array values
### 1d-array
``` python
# 1. Create an 1d-array by hand
    >>> array = [1,2,3]                             # Separate numbers by comma
    >>>
# 2. Create an 1d-array with even spacing
    >>> array_1 = np.linspace(2, 3, num=5)          # Start:2 ; End: 3 ; Total num = 5
    array([2.  , 2.25, 2.5 , 2.75, 3.  ])           # Returns an ARRAY
# 3. Reference array values
  # 3.1. Take the FIRST element, indexing starts from 0
        >>> array_1[0]   
        2.0
  # 3.2. Take the LAST element
        >>> array_1[-1]     
        3.0
  # 3.3. Get the 2nd: 4th elements
        >>> array_1[2-1:4-1]
        array([2.25, 2.5 ])
  % 3.4. Get the 2ns:last elements
        >>> array_1[2-1:]
        array([2.25, 2.5 , 2.75, 3.  ])
# 4. Get the length of array
    >>> len(array_1)    # Get the length of the 1d array
    5
```
### 2d-array
``` python
# 1. Create a 2d-array by hand
    >>> array = np.array( [[1,2],[3,4]] )                       # Separate numbers by comma
    array([[1, 2], [3, 4]])
# 2. Create 2d constant arrays
    >>> np.ones((3,3))                  # paranthesis
    array([[1., 1., 1.],
           [1., 1., 1.],
           [1., 1., 1.]])
    >>> np.zeros((3,3))                 # paranthesis
    array([[0., 0., 0.],
           [0., 0., 0.],
           [0., 0., 0.]])
# 3. Meshgrid
    >>> x = np.linspace(1,2,2)
    >>> y = np.linspace(1,3,3)
    >>> X,Y = np.meshgrid(x,y)
    >>> X
    array([[1., 2.],
           [1., 2.],
           [1., 2.]])
    >>> Y
    array([[1., 1.],
           [2., 2.],
           [3., 3.]])
# 4. Get array elements
    >>> array_2 = np.array( [[1,2,3],[4,5,6],[7,8,9]] )
    array([[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]])
    # 4.1. Take an row
        >>> array_2[0]
        array([1, 2, 3])
    # 4.2. Take an element
        >>> array_2[3-1][2-1]           # Note the output is a number
        8
    # 4.3. Take an element
        >>> array_2[0:1,0:1]            # Note the output is an array
        array([[1]])
    # 4.2. Take a sub array
        >>> array_2[0:2,0:2]
        array([[1, 2],
               [4, 5]])
# 5. Array size
    >>> X.shape
    (3,2)               # Row: 3; Col: 2
    >>> len(X)
    3                   # Only gives row
```

