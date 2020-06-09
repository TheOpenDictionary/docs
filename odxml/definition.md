# &lt;definition&gt;

Definitions are attribute-less, child-less nodes whose sole purpose is to contain a text definition, either group by a  node or by usage. While it is possible to use HTML in definition nodes, using vanilla HTML will cause the parser to treat all HTML tags as unrecognized XML children and ignore them when producing the output. Therefore, you must encode all HTML entities in your XML before compiling the file. Afterwards, you can decode these entities from the CLI output using JavaScript or your favorite coding language.

