# &lt;entry&gt;

Entries are the primary entry point to the dictionary and represent **unique terms**. They are used as lookup keys internally by ODict, so it is important there are no duplicate entries. There is a required term attribute that must be attached to every entry node that represents the word being defined.

## Attributes

| Name | Type | Required? |
| :--- | :--- | :--- |
| term | String | Yes |

## Children

| Name | Required? |
| :--- | :--- |
| [&lt;ety&gt;](ety.md) | Yes |

