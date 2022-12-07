# AvoidFieldNameMatchingMethodName
**Category:** `pmd`<br/>
**Rule Key:** `pmd:AvoidFieldNameMatchingMethodName`<br/>
> :warning: This rule is **deprecated** in favour of [S1845](https://rules.sonarsource.com/java/RSPEC-1845).

-----

It is somewhat confusing to have a field name with the same name as a method. While this is totally legal, having information (field) and actions (method) is not clear naming. Example :
<pre>
public class Foo {
  Object bar;
  // bar is data or an action or both?
  void bar() {
  }
}
</pre>
