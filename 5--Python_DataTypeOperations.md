# Different data type operations

## Dictionary
  1.  Access elements
  ```python
  >>> my_dict = {1:'apple', 2:'ball', 3:'cat'}
  ```
    - Access keys
  ```python
  >>> my_dict.keys()
  dict_keys([1, 2, 3])
  ```
    - Access values
    ```python
    >>> my_dict.values()
    dict_values(['apple', 'ball', 'cat'])
    ```
    - Access elements
    ```python
    >>> my_dict[3]
    'cat'
    >>> my_dict.get(1)
    'apple'
    ```
  2. Insert elements
  ```python
  >>> my_dict['next'] = 'dog'
  >>> my_dict
  {1: 'apple', 2: 'ball', 3: 'cat', 'next': 'dog'}
  ```

  3. Change elements
  ```python
 >>> my_dict[2] = 'bat'
 >>> my_dict
 {1: 'apple', 2: 'bat', 3: 'cat', 'next': 'dog'}
 >>> len(my_dict)
 4
  ```
