# Functions

## 1. Introductions
- High signal to ratio
- When it makes sense to create
- Similicity
- Code smells and refactoring
- Error handling
- Function and method - non-obj vs object (used interchangeably in this tutorial)

## 2. When to create a function
- Like paragraph in writing
- 4 reasons to create functions
	- Avoid Duplication (DRY)
	- Indentation is sign of complexity. 
	- Understand programmers intent. Well chosen function names instead of comments
	- Single responsibility - 1 thing and 1 thing well. Not long

## 3. Avoid Duplication
- Code is a liability. DRY, Less is more
- Look for patterns for duplication

## 4. Excessive indentation
- Arrow code. E.g. nesting of if’s. High cyclomatic complexity
	- High signal to noise
	- Complex testing
	- Comprehension decreases beyond 3 levels - arrow code.
- Eliminate arrow
	- Extract method
	- Fail fast
	- Return early

## 5. Extract Method
- Start with most deeply nested code.
- Enhances readability as readers can skip the line. e.g. Book authors moving to tables or footnotes.
	- References in texts
	- High level overview of algorithm

## 6. Return Early
- Remove deep indentation. 
	- e.g. return if username is invalid.
- Years ago it was popular to have only one return in Ruction.
	- Not today.
	- Steve McConnel - Code Complete
	- Not returning means write more code

## 7. Fail Fast
- Throw an exception as soon as an unexpected condition.
- Guard clauses - clarifies expected states for parameters
	- Safety checks at the top of method.
	- If large no. of checks, refactor to new method.
- Switch statement - have default value

## 8. Convey intend

## 9. Do one Thing
- Like paragraphs in text
- Aids the reader
- Promotes reuse
- Eases naming and testing
	- Much easier to name if does one thing
- Avoids side effects

## 10. Mayfly variables
- Initialising all variables at top.
- Mayfly - creature with very short spans. 30m to 24 hr.
- Recipe for mayfly variables
	- Initialise variables just in time
	- Do one thing

## 11. How many parameters?
- Strive for 0-2 parameters
- Easier to read, understand and test
- Helps assure function does one thing
- Watch for flag variables

## 12. What’s too long?
- Highly arbitrary measurement
- Signs that functions may be too long
	- Developers use blank lines to separate concerns
	- Too many comments
	- If scrolling is required, it may be too long
	- Naming issues - hard time coming up with a name
	- Multiple conditionals in a function
	- Hard to digest - function should work with single layer of abstraction. Rule of 7
	- Bob Martin Clean code
		- Rarely over 20 lines
		- Hardly over 100 lines
		- No more than 3 param
	- Simple functions can be longer and complex can be short
		- Linux - inversely proportional to complexity

## 13. Exceptions
- Three types of exceptions
- Unrecoverable
	- Null reference, files not found, access denied
- Recoverable
	- Retry connection
	- Try different file
	- Wait and try again
- Ignorable
	- e.g. Logging click -> Just swallow exception
- Never catch an exception that you cannot handle. Let it bubble up.
	- Correct behaviour for broken application is to crash immediately
- Replace body of try within a function to know where try starts and ends.
	- Also provides a clean name

## 14. Summary
- When to create function - duplication, indentation, unclear intent, 1 task
- Signs too long - whitespace and comments, scroll, naming issues, multiple conditionals, hard to digest e.g.excessive params
- Error handling - call function of body of try. 3 types of exceptions

