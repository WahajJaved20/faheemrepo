# Regular Expressions

Website to Cross-check REGEX -> [https://www.debuggex.com](https://www.debuggex.com)

## Meta Characters

Meta characters do not stand for themselves but instead are interpreted in some special way.

<table><thead><tr><th width="100">Meta Character</th><th>Purpose</th><th>Example Regex</th><th width="166">Working Example</th><th>Failing Example</th></tr></thead><tbody><tr><td>.</td><td>Any Single Character except a line break</td><td>ab.c</td><td>abxc</td><td>-</td></tr><tr><td>[ ]</td><td>Matches any character between the square brackets</td><td>ab[acd]f</td><td>abdf</td><td>abxf</td></tr><tr><td>[^]</td><td>Matches any character not in the square brackets</td><td>ab[^acd]f</td><td>abxf</td><td>abdf</td></tr><tr><td>*</td><td>Matches 0 or more repetitions of preceding symbol</td><td>ab*</td><td>abbbbbb</td><td>-</td></tr><tr><td>+</td><td>Matches 1 or more repetitions of preceding symbol</td><td>ab+</td><td>ab</td><td>ac</td></tr><tr><td>?</td><td>Makes preceding symbol optional</td><td>ab?</td><td>a<br>ab</td><td>-</td></tr><tr><td>{n, m}</td><td>Match at least n but not more than m repetitions of the preceding symbol</td><td>ab{2,4}</td><td>abb<br>abbb<br>abbbb</td><td>ab</td></tr><tr><td>\</td><td>Escape character, to match the already regex specified characters</td><td>ab\{</td><td>ab{</td><td>abx</td></tr><tr><td>^</td><td>Match the beginning of input</td><td>^ab</td><td>ab</td><td>fb</td></tr><tr><td>$</td><td>Match the end of input</td><td>abc$</td><td>abc</td><td>cab</td></tr><tr><td>( )</td><td>Match any character group</td><td>(a|b|c)xd</td><td>axd<br>bxd<br>cxd</td><td>dxd</td></tr></tbody></table>
