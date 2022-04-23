# Prototypes

> A partially or fully initialized object that you copy (clone) and make use of

## 1. Motivation

- an existing design (prototype)
- make a copy of the prototype and customize it.
  - requires 'deep copy' support

## 2. Prototype design parttern

- class Address

- class Person, with Person.address

- ```python
  john = Person('John')
  jane = john
  jane.name = 'name'
  # Problem: makes change in john as well
  # Why because it's a single reference to a object.
  
  ## Solution:
  jane = copy.deepcopy(john)
  ```

## 3. Prototype Factory

- class Address
- class Employee
- EmployeeFacotory



#### Summary

- To implement
  - partially construct an object or store it somewhere
  - deep copy the  prototype
  - customize resulting instance
  - Factory provides convenient API for using prototypes.



