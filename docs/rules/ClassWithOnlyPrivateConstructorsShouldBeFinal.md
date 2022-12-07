# ClassWithOnlyPrivateConstructorsShouldBeFinal
**Category:** `pmd`<br/>
**Rule Key:** `pmd:ClassWithOnlyPrivateConstructorsShouldBeFinal`<br/>
> :warning: This rule is **deprecated** in favour of [S2974](https://rules.sonarsource.com/java/RSPEC-2974).

-----

A class with only private constructors should be final, unless the private constructor is called by a inner class. Example :
<pre>
public class Foo {  //Should be final
    private Foo() { }
}
</pre>
