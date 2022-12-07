# AvoidLosingExceptionInformation
**Category:** `pmd`<br/>
**Rule Key:** `pmd:AvoidLosingExceptionInformation`<br/>
> :warning: This rule is **deprecated** in favour of [S1166](https://rules.sonarsource.com/java/RSPEC-1166).

-----

Statements in a catch block that invoke accessors on the exception without using the information only add to code size.  Either remove the invocation, or use the return result.
