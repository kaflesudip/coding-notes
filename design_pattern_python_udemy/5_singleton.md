# Singleton

## 1. Overview

- most hated design pattern
- Motivation
  - Some components make sense to be initialized only once
    - e.g. Database repository
    - Object factory
  - Why? Initializer call is expensive
  - Or resource available only available once
  - We provide everyone with same instance
  - Prevent everyone from creating copies
  - Take care of lazy instantiation
- Solution
  - A component which is intantiated only once



## 2. Singleton Allocator

```python
class Database:
	_instance = None
	
	def __new__(cls, *args, **kwargs):
		if not cls._instance:
			cls._instance = super().__new(cls, *args, **kwargs)
		return cls._instance
```

- Only good enough if nothing in `__init__`.
- May not work most time



## 3. Singleton Decorator

```python
def singleton(class_):
	instances = {}
	
	def get_instance(*args, **kwargs):
		if class_ not in instances:
			instances[class_] = class_(*args, **kwargs)
		return instances[class_]
 
@singleton
class Database:
  .......
  
```

## 4. Singleton Metaclass

- alternative to decorator

  ```python
  class Singleton(type):
    _instances = {}
    
    def __call__(cls, *args, **kwargs):
      if cls not in cls._instances:
        cls._instances[cls] = super().__call__(*arg, **kwargs)
      return cls._instances[cls]
    
  class Database(metaclass=Singleton):
    .....
  ```



## 5. Monostate

Create a shared state and assign it in `__init__`

```python
class Monostate:
  _shared_state = {}
  
  def __new__(cls, *args, **kwargs)
    obj = super().__new__(*args, **kwargs)
    obj.__dict__ = self._shared_state
    return obj
 
class CEO(Monostate):
  ....
```

- But not the best approach. Stick with metaclass or decorator



## 6. Singleton Testability

## 7. Summary

- Different realization - custom allocator, decorator or metaclass (best)

