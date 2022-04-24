# Naming


## 1. Introduction
- Why naming Is critical
- Names to avoid
- Function side effects
- Variable names

## 2. naming matters

- E..g P and M story.

## 3. Naming classes

- Dirty Names. - WebsiteBO, Utility, Common, MyFunctions
	- Magnets for lazy developers
	- Magnet classes grow to thousand lines of code as other people insert code there.
- Clean
	- User, Account, QueryBuilder
	- Single Responsibility
- Guidelines for class
	- Nouns not verbs
	- Be specific - more smaller and cohesive
		- Low cohesion means doing to many things
	- Single Responsibility
		- ProductRepository - make db query but no email
	- Avoid generic suffixes
		- Use Product not ProductInfo, ProductManager

## 4. Methods

- Method names need to read whole class before understanding.
- Bad e.g. -> get, process, pending, dolt, start, on_init, page_load etc.
- Right on - GetRegistereduser, IsValidSubmission, ImportDocument, SendEmail

## 5. Rubber Ducking

- Need a hand?
- Ask a coworker to explain and then you figure out solution
- Getting problem in naming a method / class.
- Explain what the class does outloud and then you can get a name.

## 6. Naming Warning Sign
- Watch out for - and , or,
- e.g. Save and email, process and deny.

## 7. Side Effects
- Checkpassword shouldn’t log users out.
- ValidateSubmission shouldn’t save.
- Getuser shouldn’t create session
- ChargeCreditCard shouldn’t send emails.

## 8. Abbreviations
- Abbreviations within code doesn’t make sense.
- Storage is cheap these days.
- No standard in abbreviations
- We talk about code.
	- RegUser doesn’t flow off the tongue.

## 9. Booleans
- Should sound like asking true / false questions
- Dirty - open, start, status, login
- Clean = IsOpen, done, isActive, loggedIn

## 10. Symmetry
- Opposites should be clearly opposite
- Dirty - on/disable, quick / slow, lock / open, slow / max
- On/off, fast/slow, lock/unlock. Min/max

## 11. Summary
- Strive for specific class names - lazy programmer magnet class
- The name say all - do not read to know
- Watch for nasty side-effects - no unreeled
- Booleans should sound truthy / false
- When struggling to name, verbalise to friend or duck.
