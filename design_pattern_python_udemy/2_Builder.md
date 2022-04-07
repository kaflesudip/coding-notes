# Builder

## 1 Gamma Categorization

- Design patterns are split into 3 categories
  - Creational patterns: deal with creation of patterns
- Structural Patterns
  - concerned with structures. e.g. class members
  -  stress on good API design
- Behavioral patterns
  - no central theme; all different



## 2 Builder pattern motivation

- Some objects are simple. Can be created in a single initializer.
- Other require a lot of ceremony
- having 10 init args not productive
- instead, opt for piecewise construction

When piecewise object construction is complicated, provide API for it.



## 3 Builder

- example of HTML builder

## 4 Builder Facets

```python
class PersonBuilder:
	def __init__(self, person=Person()):
		self.person = person
	
	@property
	def works(self):
		return PersonJobBuilder(self.person)
  
  @property
	def lives(self):
		return PersonAddressBuilder(self.person)
  
pb = PersonBuilder()
pb = person\
					.lives.at('london')
  				.works.at("google")
						
```

Base class jumps from one builder to other.

- Super useful but it directly violates open-close principle
  - need to go back to personbuilder to modify it

## 5 Builder interface

- we can also do it without violating open-close principle 
- inherit builders from the upper one.



## Summary

- Builder is separate component for building an object
- to make builder fluent, return self from every single method of builder.

