# dotnet-tools-settings
Setting for common tools that I used in my C# projects (like R#)


Link to .gitignore (maintained by me): https://gist.github.com/kmorcinek/2710267



## StyleCop (StyleCop Analyzers)

Rules I switch off and why:
* SA1101 - PrefixLocalCallsWithThis (remove obviousness)
* SA1111 - ClosingParenthesisMustBeOnLineOfLastParameter (rather temporary, but in some cases improves viewing history in source control)
* SA1122 - UseStringEmptyForEmptyStrings (rather temporary)
* SA1200 - UsingDirectivesMustBePlacedCorrectly (most of C# world place using outside namespace, so I don't want to fight again it)
* SA1201 - ElementsMustAppearInTheCorrectOrder (up to a team, hard to maintain always this "Order")
* SA1202 - ElementsMustBeOrderedByAccess (assume couple of public methods in class, I want to have private methods used by a public method just below this public method, not below all other public methods)
* SA1300 - ElementMustBeginWithUpperCaseLetter
* SA1309 - FieldNamesMustNotBeginWithUnderscore (private fields should begin with underscore)
* SA1310 - FieldNamesMustNotContainUnderscore (underscore are used in tests)
* SA1400 - AccessModifierMustBeDeclared (I prefer to not put "private" before private methods)
* SA1407 - ArithmeticExpressionsMustDeclarePrecedence (up to code review to make it readable, on the other hand when applying this rule R# is suggesting "remove redundant parentheses")
* SA1611 - ElementParametersMustBeDocumented (no required documentation)
* SA1615 - ElementReturnValueMustBeDocumented (no required documentation)


Rules I need to investigate more: SA1009, SA1204, SA1313, SA1516, SA1614


All rules that are not excluded here I would use for green field project and I would be changing to meet these rules in brown field project. But in brownfield sometimes allow to disable more rules "temporary", because obviously some of the require some time to spend on fixing them.
