# StdCyclomaticComplexity
**Category:** `pmd`<br/>
**Rule Key:** `pmd:StdCyclomaticComplexity`<br/>
> :warning: This rule is **deprecated** in favour of `java:MethodCyclomaticComplexity`, `java:ClassCyclomaticComplexity`.

-----

Complexity directly affects maintenance costs is determined by the number of decision points in a method plus one for the method entry. The decision points include 'if', 'while', 'for', and 'case labels' calls. Generally, numbers ranging from 1-4 denote low complexity, 5-7 denote moderate complexity, 8-10 denote high complexity, and 11+ is very high complexity.
