# Introduction

The Open Dictionary Project \(ODict for short\), is an open-source alternative to proprietary dictionary file formats [Babylon](http://www.babylon-software.com/free-dictionaries/) and [Apple Dictionaries](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/DictionaryServicesProgGuide/Introduction/Introduction.html). Similar to other dictionaries, Open Dictionary files are converted from XML \(currently in a draft specification\) to compressed, serialized, bite-sized files. ODict is built on some of the fastest technologies to ensure maximum speed when performing lookups: Google Snappy \(fastest compression\), Bleve \(fastest Go indexer\), and Flatbuffers \(fastest serialization\). Entries are searched in log\(_n_\) time.

## Motivation

ODict was developed out of the need for a fast, readily available, and open solution to cross-platform dictionary formats. Current formats such as [Apple Dictionaries](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/DictionaryServicesProgGuide/prepare/prepare.html), [Babylon](http://www.babylon-software.com/free-dictionaries/), or [StarDict](http://stardict.sourceforge.net/) dictionaries are specifically designed to work with a specific application \(usually developed by the same company that made the format\), and as a result are somewhat uni-directional \(there is official documentation on how to _write_ a dictionary in their format, but not on how to _read_ one\). This forces users to write dictionaries that only work with _one specific dictionary app_. Sure, there are scattered third-party articles online detailing these file formats and how to read them, but they are often long, convoluted, and difficult to implement yourself.

_Wouldn't it be nice if there was a completely open-source format, with documentation on both reading and writing the format, that anyone could use in **any** dictionary app?_

That's where ODict comes in.

## How It Works

ODict files are binary files, or more specifically serialized [Flatbuffers](https://google.github.io/flatbuffers/) wrapped in a [Snappy](https://github.com/google/snappy) compressor. These binary files are generated from the ODict XML markup \(ODXML for short – remember it, you'll be seeing it a lot\). Details of this markup can be found elsewhere in this documentation. These binary files are generated from the [ODict C++ compiler](https://github.com/odict/odict), which is the main application for generating, reading, and searching ODict dictionaries. Most of the other repositories in the ODict organization either convert other dictionary formats to ODXML, or allow you to read ODict dictionaries in the language of your choice \(such as [odict-java](https://github.com/odict/odict-java)\).

