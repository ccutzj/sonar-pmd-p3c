# AvoidFieldNameMatchingTypeName
**Category:** `pmd`<br/>
**Rule Key:** `pmd:AvoidFieldNameMatchingTypeName`<br/>
> :warning: This rule is **deprecated** in favour of [S1700](https://rules.sonarsource.com/java/RSPEC-1700).

-----

It is somewhat confusing to have a field name matching the declaring class name. This probably means that type and or field names could be more precise. Example :
<pre>
public class Foo extends Bar {
  // There's probably a better name for foo
  int foo;
}
</pre>
