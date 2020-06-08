# &lt;entry&gt;

Entries are the primary entry point to the dictionary and represent **unique terms**. They are used as lookup keys internally by ODict, so it is important there are no duplicate entries. There is a required term attribute that must be attached to every entry node that represents the word being defined.

## Attributes

| Name | Type | Required? |
| :--- | :--- | :--- |
| term | String | Yes |

## Child Nodes

| Name | Required? |
| :--- | :--- |
| \[Etymology\]\[ety\] | Yes |

\[ety\]: [https://www.odict.org/odxml-nodes/ety.html](https://www.odict.org/odxml-nodes/ety.html)

