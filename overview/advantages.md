# Advantages

In case you're still not sold, there are a number of advantages to using ODict over another format, given you can write or find the code required to actually use another format. Here they are.

## It's Open-Source

ODict is one of the only dictionary formats that is open-source forwards and backwards. Other dictionary apps _related_ to file formats, such as StarDict, are also open source, but require you to dig through their source code to figure out how they're reading their own format. Other formats, such as Apple Dictionaries, are completely proprietary, so you [_literally have to reverse engineer them_](https://josephg.com/blog/reverse-engineering-apple-dictionaries/) if you hope to get anything useful out of them. With ODict, you deal with none of that BS. We tell you how the file format works, show you how we process it, and give you the tools to use ODict files in your own software. It's that simple.

## It's Layout Agnostic

Many, and I mean _many_, dictionary formats rely on HTML markup to display dictionary entires. Why? Because it is the easiest. However, this places full control of dictionary layout into the hands of the _user_, which is something we don't totally agree with. We like things to be uniform, to have dictionary apps exhibit full control of how they wish to layout their entires. This way, every entry can appear the same, and continuity is ensured throughout the entire dictionary application. So how do we do it? We store all keys aspects of a dictionary entry \(etymologies, word usages, example sentences, etc.\) in a Flatbuffers schema. When you retrieve an entry, is presented as a hash table, providing only the values associated with an entry. It's up to you, the app developer, to decide how you wish to display these values.

