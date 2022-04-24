
# Principles 

## 1. Three Principles for clean code

- Right tool for the job. Technology, Data structures, 
- High signal to noise ratio
- Self-documenting (Code complete)


## 2. The Right tool for the Job
- We should use <lunatic’s favourite tool> for everything


## 3. Boundaries matter. Stay Native
- HTML, CSS, Javascript, C#, Ruby, Python etc., SQL
- HTML in JS string, JS in HTML
	- Can be tempting to use
- HTML in SQL. Presentation and data storage together.
- HTML and CSS - Inline styles
- Dynamic SQL in C# strings
- Dynamic JS in C# strings
- E.g. inject google analytic id injected in JS via. C# templete.
- Why native js -> Cached, code coloured,  syntax checking, separation of concerns, avoids string parsing, can minify and obfuscate
- Avoid using one language by other language’s string
- Rule of thumb - One language per file.

## 4. Potential Evil

- e.g. Line-to-sql in C#
- Flash / Silverlight vs Native JS
- JS in browser - validation relying


## 5. Maximize signal to Noise Ratio
- Signal is any logic that follows TED rule (Terse, Expressive, Do one thing)
- Noise
	- high cyclomatic complexity,
	- Excessive indentation
	- Huge classes
	- Long methods
	- Zombie code
	- Repetition
	- Unnecessary comments
	- No whitespaces
	- Poorly named structures
	- Overly verbose
- Why important 
	-  Our mind can only have 7 items at once.
		- Waste info. More info than they can process at once.
		- No. of methods, local variables, parameters in code. 
	- The mess builds quietly. (So good code always


## 6. DRY Principle
- Pragmatic programmer - book
- Many of same principles as relational DB normalisation
- Copy and paste often sign of design problem
- Issues:
	- Decreases signal to noise ratio (use methods and class)
	- Increases lines of code (Liability). Program by lines of code is like Aircraft by weight). Fewer lines of code means fewer bugs.
- Look for patterns and shapes


## 7. Self Documenting Code
- New devs in a team can easily navigate and understand the code.
- Strives to do 4 core things
	- Clear intent. Readers understand exactly
	- Layers of abstraction. Problem domain walked though different layers of detail
	- Format for readability
	- Favour code over comments.


## 8. Summary
- Begins with picking right tool
- Maximise Signal to noise - TED and Dry
- Self documenting code - clear intent and layers of abstraction
