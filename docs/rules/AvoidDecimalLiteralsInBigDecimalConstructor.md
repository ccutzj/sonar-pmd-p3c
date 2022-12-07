# AvoidDecimalLiteralsInBigDecimalConstructor
**Category:** `pmd`<br/>
**Rule Key:** `pmd:AvoidDecimalLiteralsInBigDecimalConstructor`<br/>
> :warning: This rule is **deprecated** in favour of [S2111](https://rules.sonarsource.com/java/RSPEC-2111).

-----

<!-- (c) 2019 PMD -->
<p>
  One might assume that the result of <code>new BigDecimal(0.1)</code> is exactly equal to <code>0.1</code>, but it is
  actually equal to <code>.1000000000000000055511151231257827021181583404541015625</code>. This is because <code>0.1</code>
  cannot be represented exactly as a double (or as a binary fraction of any finite length).
  Thus, the long value that is being passed in to the constructor is not exactly equal to 0.1, appearances notwithstanding.
</p>
<p>
  The (String) constructor, on the other hand, is perfectly predictable: <code>new BigDecimal("0.1")</code> is exactly equal
  to <code>0.1</code>, as one would expect. Therefore, it is generally recommended that the (String) constructor be used in preference to this one.
</p>
<h2>Noncompliant Code Example</h2>
<pre>
BigDecimal bd = new BigDecimal(1.123);       // loss of precision, this would trigger the rule
</pre>

<h2>Compliant Solution</h2>
<pre>
BigDecimal bd = new BigDecimal("1.123");     // preferred approach

BigDecimal bd = new BigDecimal(12);          // preferred approach, ok for integer values
</pre>
