# ODXML

ODict XML, or ODXML for short, is just a regular ol' XML file that contains the nodes needed to convert the XML into a compiled .odict file. Here's a quick example of what we're talking about:

```markup
<dictionary name="Example Dictionary 1">
    <entry term="run">
        <ety description="Latin root">
            <usage pos="verb">
                <group description="A number of verb usages">
                    <definition>(vertebrates) To move swiftly.</definition>
                    <definition>(fluids) To flow.</definition>
                    <definition>(nautical, of a vessel) To sail before the wind, in distinction from reaching or sailing close-hauled.</definition>
                    <definition>(social) To carry out an activity.</definition>
                    <definition>To extend or persist, statically or dynamically, through space or time.</definition>
                    <definition>(transitive) To execute or carry out a plan, procedure or program.</definition>
                </group>
            </usage>
            <usage pos="noun">
                <definition>Act or instance of running, of moving rapidly using the feet.</definition>
                <definition>Act or instance of hurrying (to or from a place) (not necessarily by foot); dash or errand, trip.</definition>
                <definition>A pleasure trip.</definition>
                <definition>Flight, instance or period of fleeing.</definition>
                <definition>Migration (of fish).</definition>
                <definition>A group of fish that migrate, or ascend a river for the purpose of spawning.</definition>
            </usage>
        </ety>
    </entry>
</dictionary>
```

Really easy to understand, right? By having a hierarchy of nodes, we can ensure the clarity of dictionary entries and not have dictionary developers fiddling around with inconsistent HTML code.

An explanation of what each node means can be found in the "Nodes" section.

