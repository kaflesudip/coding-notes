# Comments

## 1. Introduction
- Over reliance on comments is a code smell
- Should be a clear reason to justify existence
- Can be signal or noise
- Comments can be both great or code smell.

## 2. Necessity and a Crutch
- General rules
	- Prefer expressive code over comments. Why code updated by maintenance programmers.
	- Use comments when code alone can’t be sufficient
- Comments to avoid
	- Redundant comments
	- Intent comments
	- Apology comments

## 3. Redundant comments
- Exactly what code says.
- Like assign I to 1, instantiate a new user.
- Breaks dry principle. Need to maintain two different points
- Rules
	- Assume readers can read in language you wrote
	- DRY

## 4. Intent
- Comment to clarify magic number.
	- Can be removed
- E.g. of clarify intent in code
	- Improved function naming
	- Intermediate variable
	- Constant or enum

## 5. Apologies and Warnings
- Sorry, this crashes a lot. So, I’m swallowing the exception.
- I was too tired to refactor this pile
- Instead, don’t apologise and fix or ad TODO
- Warning comments
	- More dangerous than apologies comments
	- To avoid, refactor

## 6. Zombies code
- I’ll fix it at some point.
- Half-baked Code
- Sections of commented out code are zombie codes
- Can be difficult to comprehend
- Half dead code
- Common Causes
	- Risk Aversion -> Dev lack sense of purpose to delete unnecessary code. But code must be deleted regularly. Code is liability
	- Hoarding mentality -> Code remains in source control.
- Optimize signal to noise ratio
	- Zombie code opposes comprehension
- Hinders refactoring
- Add boise to searches
- Mental checklist
	- Any definitive day when code uncommented
	- Can be retrieved from source control
	- Can be a separate branch?
	- Enabled or disabled via. Configuration
	- Refactor ever

## 7. Dividers and Brace Trackers
- Divider comments divide into sections
	- Instead create multiple functions / methods
- Brace tracker - comments to track nested conditionals. What it’s closing
	- Alternative - refactor to a function

## 8. Bloated Header
- Boilerplate template at the top of the file.
- Filename, Author, created, summary etc.

## 9. Defect Log
- Defect some issue to fix some code

## 10. Clean comments
- TODO, Summary and Documentation
- TODO comments
	- e.g HACK api doesn’t expose needed call yet
- Tips:
	- Standardise TODO comments
	- Watch out apology, warning
	- Watch often ignored TODO
- Summary comments
	- Like beginning of book.
	- High level overview if name alone isn’t sufficient to convey
- DoC comments
	- See factbook.com/api for documentation

## 11. Summary
- Comments are useful but alternatives may be better
- Ask
	- If an be expressed in code
		- Intermediate variable
		- Eliminate magic number
		- Utilize enum
	- Recaotr to well-named method
	- Am I explain bad code that needs refactoring
	- Should this simply be a message in source code commit?
