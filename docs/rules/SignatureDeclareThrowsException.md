# SignatureDeclareThrowsException
**Category:** `pmd`<br/>
**Rule Key:** `pmd:SignatureDeclareThrowsException`<br/>
> :warning: This rule is **deprecated** in favour of [S112](https://rules.sonarsource.com/java/RSPEC-112).

-----

It is unclear which exceptions that can be thrown from the methods. It might be difficult to document and understand the vague interfaces. Use either a class derived from RuntimeException or a checked exception.
