# FieldDeclarationsShouldBeAtStartOfClass
**Category:** `pmd`<br/>
**Rule Key:** `pmd:FieldDeclarationsShouldBeAtStartOfClass`<br/>
> :warning: This rule is **deprecated** in favour of [S1213](https://rules.sonarsource.com/java/RSPEC-1213).

-----

Fields should be declared at the top of the class, before any method declarations, constructors, initializers or inner classes. Example:
<pre>
public class HelloWorldBean {

  // Field declared before methods / inner classes - OK
  private String _thing;

  public String getMessage() {
    return "Hello World!";
  }

  // Field declared after methods / inner classes - avoid this
  private String _fieldInWrongLocation;
}
</pre>
