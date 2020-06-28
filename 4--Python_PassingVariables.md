# Function with **variable** inputs
  ## 1. *kwag
  ```python
  def person(name, *data):
    print(name)
    print(data)

  > person('chun', 26, 'Orlando', 4584958945)
        chun
        (26, 'Orlando', 4584958945)  
  ```

  ## 2. **kwag : Keyworded variable length argument
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
