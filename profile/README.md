# BinaryHeart Organization Wide Contribution Guidelines 

## Purpose
This document exists to document standards for all members of BinaryHeart to contribute within our GitHub organization. Additional documents on applying the guidelines can be found in the “.github” repository. If you're a member who'd like to contribute, create an issue to detail what you'd like to add/amend.


## AI Usage
1. You, the person(s) committing the code, are entirely responsible and liable for the impact of the code, regardless of if it was handwritten or AI generated.
2. Always disclose AI tool usage, regardless of breadth of usage.
    1. Everything from writing an entire feature to fixing a minor bug should be disclosed in the resulting PR.
    2. Disclose what you told any AI tools to do and why. You cannot just say “(AI tool) told me to do…”, share any back and forth that preceded decision making.
    3. Remember: AI is not a co-author, it is a tool. You are still responsible for how this tool is used.
3. The entire development process may not be fully agentic.
    1. You must create your own PRs, and they must be reviewed and approved prior to merging.
    2. You must be involved throughout the process, reviewing the output of any agent/tool used.
4. Never allow an AI tool to include personal data/information. Always fill this in by hand. You should be aware of any and all personal information you have contributed.
    1. Never input personal data directly into an AI tool. This includes names, photos, phone numbers, addresses, birthdates, etc.
    2. If you are unsure of whether something is considered personal data/information, defer to [GDPR Article 4](https://gdpr-info.eu/art-4-gdpr/).
5. If you are not the sole author of your code, you must be able to explain and justify any code you are contributing within the organization.
    1. Merely citing comments, readmes, and other documentation/justifications not authored by you may not be used in lieu of understanding what you are trying to contribute.

## Code Standards/Style
1. When adding new code, first ensure that your feature/problem/other that you’re working on will be implemented in a simple and secure manner. Time permitting, sanity check with another developer to avoid wasting time on bad solutions.
2. When adding new code, maintain the style in use for this language. If set up, follow the Prettier rules for the repository. 
    1. Remember that style exists beyond variable naming and whitespace. How you write code should be consistent with existing code. 
    2. Examples:
        1. Continue using camelCase, kebab-case, or snake_case if it’s already in use for this language across other files. 
        2. In TypeScript, never use var, instead opt for const and let which are block scoped.
3. If working on a new file in a new language and unsure of general guidelines, refer to Google’s style guidelines for the language.
4. Always use comments to explain why something is being done. With brevity, provide a thorough explanation that is as succinct as possible. 
    1. As needed, use comments to explain what is being done. At minimum, this should be done when using newer/uncommon language features.
    2. If you aren’t sure of whether some code warrants commenting, think of yourself from 3 months in the future and do what is kind.
5. Never abstract for fun. If an abstraction is not immediately needed to address some problem, don’t abstract.
6. Apply fault tolerant techniques such that code fails gracefully. If working in a language that supports exception handling, use this, and gracefully exit as a last resort.
7. If and only if you cannot recover from a program failure, return an error such that:
    1. The contents of the error message are helpful and allow someone to quickly know what went wrong.
    2. The error can be traced to the relevant file(s), method(s), and line(s) of code. 
8. When fixing bugs, first write test cases to verify the expected output. After you have fixed the bug, run the tests against the new code. If and only if all tests pass is the bug considered fixed.

## Communication/Other
1. [Write good commit messages](https://cbea.ms/git-commit/).
2. When writing bug reports, include the following in the given order (italicized items are optional):
    1. One line summary
        1. Include what happened, where it happened, and the circumstances where it happened
    2. Expected behavior
    3. *Environment where the bug occurred*
    4. *How the bug was found*
    5. Steps to reproduce the bug
    6. Importance level, i.e. how soon should this be addressed
    7. Severity level, i.e. how problematic is this bug
    8. *Comments (thoughts on the potential cause, other details that don’t fit above, etc)*