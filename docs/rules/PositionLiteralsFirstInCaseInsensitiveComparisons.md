# PositionLiteralsFirstInCaseInsensitiveComparisons
**Category:** `pmd`<br/>
**Rule Key:** `pmd:PositionLiteralsFirstInCaseInsensitiveComparisons`<br/>
> :warning: This rule is **deprecated** in favour of [S1132](https://rules.sonarsource.com/java/RSPEC-1132).

-----

Position literals first in comparisons, if the second argument is null then NullPointerExceptions
can be avoided, they will just return false. Example:
<pre>
class Foo {
  boolean bar(String x) {
    return x.equalsIgnoreCase("2"); // should be "2".equalsIgnoreCase(x)
  }
}
</pre>
