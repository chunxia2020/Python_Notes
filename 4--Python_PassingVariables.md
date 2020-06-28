# Function with **variable** inputs, *kwag type is tuple
  ## 1. *kwag
  ```python
  def person(name, *data):
    print(name)
    print(data)   # data type is tuple

  > person('chun', 26, 'Orlando', 4584958945)
        chun
        (26, 'Orlando', 4584958945)  
  ```

  ## 2. **kwag : Keyworded variable length argument, **kwag type is dict
  ```python
  def person(name, **data):
    print(name)
    for key, value in data.items():
      print(key, value)

  > person('chun', age=26, city='Orlando', num=4584958945)
        chun
        age 26
        city Orlando
        num 4584958945  
  ```
