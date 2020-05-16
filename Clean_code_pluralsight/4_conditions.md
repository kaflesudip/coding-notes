# 4 Conditions

## 1. Introduction
- 4 simple principles
- Clear intent. Why we made the decision to go in given direction
- Use the right tool. 
- Bite-size logic. Mind can comprehend
- Sometimes code isn’t the answer. Remove conditionals 

## 2. Boolean comparisons
- Obvious choice when true / false.
- Dirty if (loggedIn == True)
- Good if (logged)

## 3. Boolean Assignments
- Boolean should be assigned implicity.
- e.g. Use IsForLunch = cashToWaller > 6.00. Instead of if
	- Fewer lines
	- No separate initialisation
	- No repetition
	- Reads like speech (Otherwise overly wordy)

## 4. Positive Conditions
- Dirty if (!isNotLoggedIn). Cognitive load is increased
- Use positive conditionals
- Clean - if (loggedIn)

## 5. Ternary Elegance
- Int registrationFee = isSpeaker ? 0 : 50;
- Easier to pass by for users scanning the code. 
- Honours DRY principle. No need to repeat the variable.
- YAGNEE - You Aren’t Gonna Need it.
	- No need to add complexity for future.
- Bad - Multiple ternary operator in single 

## 6. Stringly Typed
- Avid being “Stringly” typed.
- Dirty
	- If (employeeType == ‘manager’)
- Clean
	- If (employee.Type == EmployeeType.Manager.
	- Use nom
- Strongly typed => No types
- Intellisense support
- Document states - potential states finite. I can see. Not possible with strings
- Searchable

## 7. Magic Numbers
- Sally went to #12 dealer to by a #12
- Sally went to the Ferrari dealer to buy a Enzo.
- If (age > 21>
	- Why dev. Typed 21 here?
	- Numbers wrong tools for conditionals
- Const int legalDrinkingAge = 21;
- If (age > legalDrinkginAge)
- Or use Enums
	- If (status==2) // Dirty
	- If (status == status.Active) // clean
- Clarifies intent

## 8. Complex conditionals
- Multipel and and or.
- Before they grow out of control. Use 2 tactics
	- Intermediate variables
	- Encapsulate via. Function

## 9. Polymorphism vs Enums
- Favour polymorphism over enums for Behavior
- Abstract base class and encapsulate.

## 10. Be Declarative.
- Linkedin objects in C#.
- Similar to filter.
- Python Pynq.

## 11. Table Driven Methods
- Hard coding. Use database tables instead

## 12. Summary
- Strive for clear intend without comments
- Strongly typed via. Constants and enums
- Be declarative than interactive.
- Consider leveraging db -> table driven
