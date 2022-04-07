# SOLID design principles

- Robert C. Martin (Uncle Bob)

# 1 Single responsibility principle (SRP)

- SOC (separation of concern)
- class:
  - has primary responsibility
  - should not take other responsibilities

```python
class Journal:
    def __init__(self):
        self.entries = []
        self.count = 0

    def add_entry(self, text):
        self.entries.append(f"{self.count}: {text}")

    def remove_entry(self, pos):
        pass

    # break SRP
    def save(self, filename):
        file = open(filename, "w")
        file.write(str(self))
        file.close()

    def load(self, filename):
        pass

    def load_from_web(self, uri):
        pass
```

- Why save breaks SRP?
  - persistance handled here. Need to change every class if method changes
  - Solution: take responsibility of persistance in a separate class

```python
class PersistenceManager:
    def save_to_file(journal, filename):
        file = open(filename, "w")
        file.write(str(journal))
        file.close()
```

### Takeaway

- Do not overload.
- Antipattern: God object, everything in a single class



## 2 Open-closed principle

Classes should be open for extension and closed for modification

### Example:

1. We have a class `ProductFilter`
2. Implement method to `filter_by_color`.
3. Goes to production.
4. Want to add filter by size.
5. You add another method `filter_by_size`.

#### Violates Open-closed principle

**Why?** Classes should be extended not modified.

May need more methods.

- `filter_by_size_and_color`, `filter_by_size_or_color`

#### Solution: 

- Use enterprise pattern - `Specification`

**Takeaway**

Don't want to mess up class already in production



## 3 Liskov Substitution principle (LSP)

You should be able to substitue a base type for a subtype

- a function works on base class but not on derived class
  - inheriting `Rectangle` class to make `Square`

> Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it 

## 4 Interface Segregation principle (ISP)

- do not stick too many elements into an interface

### Example

- Create a `Machine` class with methods `print`, `fax`, `scan`  Raise `NotImplemented` error.
- A class like `MultiFunction` printer needs all methods.
- But what about a `OldFashionedPrinter`. It cannot implement fax.
  - Either `pass` OR
  - Raise `NotImplemented` error

### Idea of ISP

- keep things granular instead of keeping everything
- Instead of `Machine` class create `Printer` class
  - create `print` method
- Another class called `Scanner`
  - Implement `span` method
- Combine two classes or use just one.

### Takeaway

Creating Interface with too many methods is not a good idea. Split into smallest interface, so that people do not need to implement more than they need to.

## 5 Dependency Inversion Principle (DIP)

- Not related to dependency injection.

- High level classes should not depend on low level modules. Instead they should depend on `abstraction` i.e. on `abstract`methods or classes.

### Example

- define `Person`
- define `Relationsship`
  - add an attribute `relations` as a list.
- define `Research`
  - Uses `relations` list to print relations between two `Person` in `Relation`
- Problem: If `relations` is changed to a different data structure, `Research` doesn't work.

#### Solution

- Do not depend on concreate implementation of `relations` as list.
- create methods like `find_all_children`

## Summary

- Single Responsibiility Principle - A class should only have one reason to change
  - Separtion of concerns
- Open-closed principle 
  - Classes: open for extension but closed for modification
- Liskov Substitution Principle
  - Able to substitute base type for a subtype
- Interface Segregation Principle
  - Do not put too much into single interface
  - YAGNI - You Ain't Going to need it
- Dependency Inversion Principle
  - High-level modules should not depend on low-level ones; use abstractions

