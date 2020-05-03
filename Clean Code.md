# Clean Code

## 1 Introductions

### # Why Should I care?

- If you cannot **justify** cleanliness of code, there are chances of change.
- Writing code is easy, **reading** is hard.
- **Technical debt **is depressing. Drives talent elsewhere from organisation.
- You are **lazy**. Good kind of lazy. Extra care upfront so that not hard later.
- No time to be **sloppy**. Bob Martin - Clean code. Boss - speed, dev chose right. Clean code and fast both at same time.
- **Don’t be a verb. **Previous developers may be named as verb

**
**
**### # The Foundation
**
- Clean Code
- SOLID Code
- Auto Testing - Legacy code is any code without testing.
- Refactoring
- DDD, TDD and Design Patterns.

**
**
**# Congratulations you’re an author**
- Each line of code read by humans 10+ times
- Great authors write books to convey clear story.
- Use chapter, header, paragraph.
- Developer - namespace, classes and methods

### # Comparisons

- Verbalize code (Reading code aloud)

### # Resources

- Code Complete (Highest voted on SO)
- Robert C Martin - Clean code (Uncle Bob)
- The Pragmatic Prgrammer - Andrew Hunt

## 2 Principles 

### # Three Principles for clean code

- Right tool for the job. Technology, Data structures, 
- High signal to noise ratio
- Self-documenting (Code complete)

**
**
**# The Right tool for the Job**
- We should use <lunatic’s favourite tool> for everything

**
**
**# Boundaries matter. Stay Native**
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
- **Rule of thumb - One language per file.**

### # Potential Evil

- e.g. Line-to-sql in C#
- Flash / Silverlight vs Native JS
- JS in browser - validation relying

**# Maximize signal to Noise Ratio**
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

**
**
**# DRY Principle**
- Pragmatic programmer - book
- Many of same principles as relational DB normalisation
- Copy and paste often sign of design problem
- Issues:
	- Decreases signal to noise ratio (use methods and class)
	- Increases lines of code (Liability). Program by lines of code is like Aircraft by weight). Fewer lines of code means fewer bugs.
- Look for patterns and shapes

**
**
**# Self Documenting Code**
- New devs in a team can easily navigate and understand the code.
- Strives to do 4 core things
	- Clear intent. Readers understand exactly
	- Layers of abstraction. Problem domain walked though different layers of detail
	- Format for readability
	- Favour code over comments.

**
**
**# Summary**
- Begins with picking right tool
- Maximise Signal to noise - TED and Dry
- Self documenting code - clear intent and layers of abstraction

**
**
**
**
**## 3 Naming
**
**
**
**# Introduction**
- Why naming Is critical
- Names to avoid
- Function side effects
- Variable names

### # naming matters

- E..g P and M story.

# Naming classes
- Dirty Names. - WebsiteBO, Utility, Common, MyFunctions
	- Magnets for lazy developers
	- Magnet classes grow to thousand lines of code as other people insert code there.
- Clean
	- User, Account, QueryBuilder
	- Single Responsibility
- **Guidelines for class**
	- Nouns not verbs
	- Be specific - more smaller and cohesive
		- Low cohesion means doing to many things
	- Single Responsibility
		- ProductRepository - make db query but no email
	- Avoid generic suffixes
		- Use Product not ProductInfo, ProductManager

### # Methods

- Method names need to read whole class before understanding.
- Bad e.g. -> get, process, pending, dolt, start, on_init, page_load etc.
- Right on - GetRegistereduser, IsValidSubmission, ImportDocument, SendEmail

### # Rubber Ducking

- Need a hand?
- Ask a coworker to explain and then you figure out solution
- Getting problem in naming a method / class.
- Explain what the class does outloud and then you can get a name.

# Naming Warning Sign
- Watch out for - and , or,
- e.g. Save and email, process and deny.

# Side Effects
- Checkpassword shouldn’t log users out.
- ValidateSubmission shouldn’t save.
- Getuser shouldn’t create session
- ChargeCreditCard shouldn’t send emails.

# Abbreviations
- Abbreviations within code doesn’t make sense.
- Storage is cheap these days.
- No standard in abbreviations
- We talk about code.
	- RegUser doesn’t flow off the tongue.

# Booleans
- Should sound like asking true / false questions
- Dirty - open, start, status, login
- Clean = IsOpen, done, isActive, loggedIn

# Symmetry
- Opposites should be clearly opposite
- Dirty - on/disable, quick / slow, lock / open, slow / max
- On/off, fast/slow, lock/unlock. Min/max

# Summary
- Strive for specific class names - lazy programmer magnet class
- The name say all - do not read to know
- Watch for nasty side-effects - no unreeled
- Booleans should sound truthy / false
- When struggling to name, verbalise to friend or duck.

## 4 Conditions

# Introduction
- 4 simple principles
- **Clear intent.** Why we made the decision to go in given direction
- **Use the right tool. **
- **Bite-size logic**. Mind can comprehend
- **Sometimes code isn’t the answer. **Remove conditionals 

# Boolean comparisons
- Obvious choice when true / false.
- Dirty if (loggedIn == True)
- Good if (logged)

# Boolean Assignments
- Boolean should be assigned implicity.
- e.g. Use IsForLunch = cashToWaller > 6.00. Instead of if
	- Fewer lines
	- No separate initialisation
	- No repetition
	- Reads like speech (Otherwise overly wordy)

# Positive Conditions
- Dirty if (!isNotLoggedIn). Cognitive load is increased
- Use positive conditionals
- Clean - if (loggedIn)

# Ternary Elegance
- Int registrationFee = isSpeaker ? 0 : 50;
- Easier to pass by for users scanning the code. 
- Honours DRY principle. No need to repeat the variable.
- YAGNEE - You Aren’t Gonna Need it.
	- No need to add complexity for future.
- Bad - Multiple ternary operator in single 

# Stringly Typed
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

# Magic Numbers
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

# Complex conditionals
- Multipel and and or.
- Before they grow out of control. Use 2 tactics
	- Intermediate variables
	- Encapsulate via. Function

# Polymorphism vs Enums
- Favour polymorphism over enums for Behavior
- Abstract base class and encapsulate.

# Be Declarative.
- Linkedin objects in C#.
- Similar to filter.
- Python Pynq.

# Table Driven Methods
- Hard coding. Use database tables instead

# Summary
- Strive for clear intend without comments
- Strongly typed via. Constants and enums
- Be declarative than interactive.
- Consider leveraging db -> table driven

## 5 Functions

# Introductions
- High signal to ratio
- When it makes sense to create
- Similicity
- Code smells and refactoring
- Error handling
- Function and method - non-obj vs object (used interchangeably in this tutorial)

# When to create a function
- Like paragraph in writing
- 4 reasons to create functions
	- Avoid Duplication (DRY)
	- Indentation is sign of complexity. 
	- Understand programmers intent. Well chosen function names instead of comments
	- Single responsibility - 1 thing and 1 thing well. Not long

# Avoid Duplication
- Code is a liability. DRY, Less is more
- Look for patterns for duplication

# Excessive indentation
- Arrow code. E.g. nesting of if’s. High cyclomatic complexity
	- High signal to noise
	- Complex testing
	- Comprehension decreases beyond 3 levels - arrow code.
- Eliminate arrow
	- Extract method
	- Fail fast
	- Return early

# Extract Method
- Start with most deeply nested code.
- Enhances readability as readers can skip the line. e.g. Book authors moving to tables or footnotes.
	- References in texts
	- High level overview of algorithm

# Return Early
- Remove deep indentation. 
	- e.g. return if username is invalid.
- Years ago it was popular to have only one return in Ruction.
	- Not today.
	- Steve McConnel - Code Complete
	- Not returning means write more code

# Fail Fast
- Throw an exception as soon as an unexpected condition.
- Guard clauses - clarifies expected states for parameters
	- Safety checks at the top of method.
	- If large no. of checks, refactor to new method.
- Switch statement - have default value

# Convey intend

# Do one Thing
- Like paragraphs in text
- Aids the reader
- Promotes reuse
- Eases naming and testing
	- Much easier to name if does one thing
- Avoids side effects

# Mayfly variables
- Initialising all variables at top.
- Mayfly - creature with very short spans. 30m to 24 hr.
- Recipe for mayfly variables
	- Initialise variables just in time
	- Do one thing

# How many parameters?
- Strive for 0-2 parameters
- Easier to read, understand and test
- Helps assure function does one thing
- Watch for flag variables

# What’s too long?
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

# Exceptions
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

# Summary
- When to create function - duplication, indentation, unclear intent, 1 task
- Signs too long - whitespace and comments, scroll, naming issues, multiple conditionals, hard to digest e.g.excessive params
- Error handling - call function of body of try. 3 types of exceptions

**6 Classes**

# Intro
- Not a course on OOP. Instead go for SOLID principles, Design Patterns
- Agenda
	- When to create a class
	- Cohesive classes
	- Organisation of logic and flow
	- Primitive obsession
	- Outline Rule to speed read classes

# When to create
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

# Cohesion
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

# When a class is too small
- Ever complain that a class is too small? Very rare
- Few signs
	- Two class rely on each other heavily. Inappropriate intimacy
	- Feature envy
	- Too many pieces
- But these issues may be unicorns in real world

# Primitive Obsession
- e.g. passing 7+ arguments instead of object into a method.
- Clean -> pass object as param
	- Helps reader to conceptualise
	- Implicit -> explicit
	- Encapsulation
	- Aids maintenance

# Principle of Proximity
- Strive to make code read top to bottom when possible
- Keep related actions together
- Loose rule

# The outline Rule
- Collapsed code should look like an outline
- Strive for multiple layers of abstraction

# Summary
- Cohesion - strongly related methods
- Watch out for primitive obsession 
- Organise to read top=bottom when possible
- Place related code together
- Multi-layer abstraction using outline rule

## 7 Comments

# Introduction
- Over reliance on comments is a code smell
- Should be a clear reason to justify existence
- Can be signal or noise
- Comments can be both great or code smell.

# Necessity and a Crutch
- General rules
	- Prefer expressive code over comments. Why code updated by maintenance programmers.
	- Use comments when code alone can’t be sufficient
- Comments to avoid
	- Redundant comments
	- Intent comments
	- Apology comments

# Redundant comments
- Exactly what code says.
- Like assign I to 1, instantiate a new user.
- Breaks dry principle. Need to maintain two different points
- Rules
	- Assume readers can read in language you wrote
	- DRY

# Intent
- Comment to clarify magic number.
	- Can be removed
- E.g. of clarify intent in code
	- Improved function naming
	- Intermediate variable
	- Constant or enum

# Apologies and Warnings
- Sorry, this crashes a lot. So, I’m swallowing the exception.
- I was too tired to refactor this pile
- Instead, don’t apologise and fix or ad TODO
- Warning comments
	- More dangerous than apologies comments
	- To avoid, refactor

# Zombies code
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

# Dividers and Brace Trackers
- Divider comments divide into sections
	- Instead create multiple functions / methods
- Brace tracker - comments to track nested conditionals. What it’s closing
	- Alternative - refactor to a function

# Bloated Header
- Boilerplate template at the top of the file.
- Filename, Author, created, summary etc.

# Defect Log
- Defect some issue to fix some code

# Clean comments
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

# Summary
- Comments are useful but alternatives may be better
- Ask
	- If an be expressed in code
		- Intermediate variable
		- Eliminate magic number
		- Utilize enum
	- Recaotr to well-named method
	- Am I explain bad code that needs refactoring
	- Should this simply be a message in source code commit?

## 7 DEMO

# Introduction
- App -> speaker registration

## 8 Stay Clean

# When to Refactor
- If it’s not broken, don’t fix
- When to
	- It should be the code that you are currently working with
	- Difficult to comprehend or change for you
	- Test coverage to protect from regression

# Broken windows
- Accept no broken windows.
- A building with few broken windows have tendencies for others to break in and break more.
- Do not allow mistakes of past to open door for more mistakes

# Code reviews and Pair programming
- Promote proactive cleanliness
- Set guidelines
- Work in pairs
	- Real-time code review
	- Increases quality
	- Naming and refactoring easier

# Boy Scout Rule
- Rober C. martin. - 

# Conclusion
- Refactor when necessary. Not every code we see
- Set and maintain standards
- Do code reviews and watch for broken windows
- Pair and share your knowledge
- Leave the code a better litter than you found it

