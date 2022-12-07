# AvoidMultipleUnaryOperators
**Category:** `pmd`<br/>
**Rule Key:** `pmd:AvoidMultipleUnaryOperators`<br/>
> :warning: This rule is **deprecated** in favour of [S881](https://rules.sonarsource.com/java/RSPEC-881).

-----

Using multiple unary operators may be a bug, and/or is confusing. Check the usage is not a bug, or consider simplifying the expression. Example :
<pre>
// These are typo bugs, or at best needlessly complex and confusing:
int i = - -1;
int j = + - +1;
int z = ~~2;
boolean b = !!true;
boolean c = !!!true;

// These are better:
int i = 1;
int j = -1;
int z = 2;
boolean b = true;
boolean c = false;

// And these just make your brain hurt:
int i = ~-2;
int j = -~7;
</pre>
