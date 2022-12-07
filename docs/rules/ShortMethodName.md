# ShortMethodName
**Category:** `pmd`<br/>
**Rule Key:** `pmd:ShortMethodName`<br/>
> :warning: This rule is **deprecated** in favour of [S100](https://rules.sonarsource.com/java/RSPEC-100).

-----

Detects when very short method names are used. Example :
<pre>
public class ShortMethod {
  public void a( int i ) { // Violation
  }
}
</pre>
