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
>>> array_2d
```
