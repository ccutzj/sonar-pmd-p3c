# SwitchStmtsShouldHaveDefault
**Category:** `pmd`<br/>
**Rule Key:** `pmd:SwitchStmtsShouldHaveDefault`<br/>
> :warning: This rule is **deprecated** in favour of `java:SwitchLastCaseIsDefaultCheck`.

-----

Switch statements should have a default label. Example :
<pre>
public class Foo {
 public void bar() {
  int x = 2;
  switch (x) {
   case 2: int j = 8;
  }
 }
}
</pre>
