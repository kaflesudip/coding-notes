# Classes

## 1. Intro
- Not a course on OOP. Instead go for SOLID principles, Design Patterns
- Agenda
	- When to create a class
	- Cohesive classes
	- Organisation of logic and flow
	- Primitive obsession
	- Outline Rule to speed read classes

## 2. When to create
- Thinking like authors, classes are like heading in the book.
	- Make book more scannable
	- Single responsibility
- New concept -> Abstract or real-world concept.
- Low cohesion
	- Methods should relate
- Promote Reuse
	- Small, targeted => reuse
- Reduce complexity
	- Solve once, hide away
- Clarify parameters
	- Identify a group of data

## 3. Cohesion
- e.g. Theatre used as a parking lot.
- When assign wrong responsibility to a single class or very generic common
- Strongly-related responsibilities
	- Enhances readability
	- Increases likelihood of reuse
	- Avoids attracting the lazy (magnet classes) [Steve smith - solid principles]
- Watch out for
	- Methods that don’t interact with the rest of he class
	- Fields that are only used by one method
		- Related functionality extracted to separate class
	- Classes that change often- use source control as a hint
- Low cohesion vehicle
	- Vehicle -> edit vehicle options, update pricing, schedule maintenance, send maintenance reminder, select financing, calculate monthly payment
- High cohesion
	- Vehicle -> Edit vehicle options and pricing
	- VehicleMaintenance - Schedule maintenance, send maintenance reminder
- VehicleFinance
	- Select Financing
	- Calculate monthly payment
- Names are so important for high cohesion
- Noun, specific names

## 4. When a class is too small
- Ever complain that a class is too small? Very rare
- Few signs
	- Two class rely on each other heavily. Inappropriate intimacy
	- Feature envy
	- Too many pieces
- But these issues may be unicorns in real world
## 5. Primitive Obsession
- e.g. passing 7+ arguments instead of object into a method.
- Clean -> pass object as param
	- Helps reader to conceptualise
	- Implicit -> explicit
	- Encapsulation
	- Aids maintenance

## 6. Principle of Proximity
- Strive to make code read top to bottom when possible
- Keep related actions together
- Loose rule

## 7. The outline Rule
- Collapsed code should look like an outline
- Strive for multiple layers of abstraction

## 8. Summary
- Cohesion - strongly related methods
- Watch out for primitive obsession 
- Organise to read top=bottom when possible
- Place related code together
- Multi-layer abstraction using outline rule
