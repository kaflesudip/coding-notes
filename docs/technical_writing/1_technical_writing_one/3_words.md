# Words

[https://developers.google.com/tech-writing/one/words](https://developers.google.com/tech-writing/one/words)

## 1. Define new or unfamilier terms

- Recognize words / terms unfamilier to target audience
- One of following two tactics
    - If exists, link (don't reinvent)
    - If doc introduces, define. If many terms, create glossary.

## 2. Use terms consistently

> If you change the name of a variable midway through a method, your code won’t compile. Similarly, if you rename a term in the middle of a document, your ideas won’t compile (in your users’ heads).

### Bad (Used both Protocol buffers and protobuf)

> **Protocol Buffers** provide their own definition language. Blah, blah, blah. And that's why **protobufs** have won so many county fairs.

### Good

> Protocol Buffers (or protobufs for short) provide their own definition language. Blah, blah, blah. And that's why protobufs have won so many county fairs.


## 3. Use acronyms properly

- Initial use - spell full term, acronym in paranthesis.
- Bad - cycling between acronym and full term
- Should you use acronyms?
   - last layer of abstraction
   - If not used few times, don't define acronyms
   - Define if i) if very short than full ii) used frequently


## 4. Disambiguate pronouns

- Pronouns to nouns - pointers in programming
- improper - cognitive equivalent to null pointer
- Many cases - avoid and just reuse noun
- When to use
  - only after introducing noun
  - Placement - close to referring noun
  - More than 5 words between noun and pronoun, repeat noun
  - 2nd noun in between. Reuse noun.


### Confusing It and they

- it / they, them, and their.
- e.g. python or C++?

	> Python is interpreted, while C++ is compiled. It has an almost cult-like following.

- they

	> Be careful when using Frambus or Carambola with HoobyScooby or BoiseFram because a bug in their core may cause accidental mass unfriending.

- this and that
	> You may use either Frambus or Foo to calculate derivatives. This is not optimal.

#### Solution to using it and they
- Replace it and they with noun
- Place noun immediately after it and they

	> Overlapping functionality is not optimal.
	
	OR

	> This overlapping functionality is not optimal.




