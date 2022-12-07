# AvoidProtectedMethodInFinalClassNotExtending
**Category:** `pmd`<br/>
**Rule Key:** `pmd:AvoidProtectedMethodInFinalClassNotExtending`<br/>
> :warning: This rule is **deprecated** in favour of [S2156](https://rules.sonarsource.com/java/RSPEC-2156).

-----

Do not use protected methods in most final classes since they cannot be subclassed. This should
only be allowed in final classes that extend other classes with protected methods (whose
visibility cannot be reduced). Clarify your intent by using private or package access modifiers instead. Example:
<pre>
public final class Foo {
  private int bar() {}
  protected int baz() {} // Foo cannot be subclassed, and doesn't extend anything, so is baz() really private or package visible? 
}
</pre>
