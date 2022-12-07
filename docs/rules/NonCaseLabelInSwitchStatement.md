# NonCaseLabelInSwitchStatement
**Category:** `pmd`<br/>
**Rule Key:** `pmd:NonCaseLabelInSwitchStatement`<br/>
> :warning: This rule is **deprecated** in favour of [S1219](https://rules.sonarsource.com/java/RSPEC-1219).

-----

A non-case label (e.g. a named break/continue label) was present in a switch statement. This legal, but confusing. It is easy to mix up the case labels and the non-case labels.
