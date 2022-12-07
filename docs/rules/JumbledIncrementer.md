# JumbledIncrementer
**Category:** `pmd`<br/>
**Rule Key:** `pmd:JumbledIncrementer`<br/>
> :warning: This rule is **deprecated** in favour of `java:ForLoopCounterChangedCheck`.

-----

Avoid jumbled loop incrementers - it's usually a mistake, and it's confusing even if it's what's intended.
<br>Example :
<pre>
public class JumbledIncrementerRule1 {
  public void foo() {
   for (int i = 0; i < 10; i++) {
    for (int k = 0; k < 20; i++) {
     System.out.println("Hello");
    }
   }
  }
}</pre>
