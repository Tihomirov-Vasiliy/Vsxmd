<a name='assembly'></a>
# Vsxmd

## Contents

- [AssemblyUnit](#AssemblyUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
- [BaseUnit](#BaseUnit `type`)
  - [#ctor(element,elementName)](##ctor(element,elementName) `constructor`)
  - [Element](#Element `property`)
  - [ElementContent](#ElementContent `property`)
  - [GetAttribute(name)](#GetAttribute(name) `method`)
  - [GetChild(name)](#GetChild(name) `method`)
  - [GetChildren(name)](#GetChildren(name) `method`)
  - [ToMarkdown()](#ToMarkdown() `method`)
- [Converter](#Converter `type`)
  - [#ctor(document)](##ctor(document) `constructor`)
  - [ToMarkdown(document)](#ToMarkdown(document) `method`)
  - [ToMarkdown()](#ToMarkdown() `method`)
- [ExampleUnit](#ExampleUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(element)](#ToMarkdown(element) `method`)
- [ExceptionUnit](#ExceptionUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(elements)](#ToMarkdown(elements) `method`)
- [Extensions](#Extensions `type`)
  - [AsCode(code)](#AsCode(code) `method`)
  - [Escape(content)](#Escape(content) `method`)
  - [Join(value,separator)](#Join(value,separator) `method`)
  - [NthLast\`\`1(source,index)](#NthLast\`\`1(source,index) `method`)
  - [Suffix(value,suffix)](#Suffix(value,suffix) `method`)
  - [TakeAllButLast\`\`1(source,count)](#TakeAllButLast\`\`1(source,count) `method`)
  - [ToAnchor(href)](#ToAnchor(href) `method`)
  - [ToHereLink(href)](#ToHereLink(href) `method`)
  - [ToLowerString(memberKind)](#ToLowerString(memberKind) `method`)
  - [ToMarkdownText(element)](#ToMarkdownText(element) `method`)
  - [ToReferenceLink(memberName,useShortName)](#ToReferenceLink(memberName,useShortName) `method`)
- [IConverter](#IConverter `type`)
  - [ToMarkdown()](#ToMarkdown() `method`)
- [IUnit](#IUnit `type`)
  - [ToMarkdown()](#ToMarkdown() `method`)
- [MemberKind](#MemberKind `type`)
  - [Constants](#Constants `constants`)
  - [Constructor](#Constructor `constants`)
  - [Method](#Method `constants`)
  - [NotSupported](#NotSupported `constants`)
  - [Property](#Property `constants`)
  - [Type](#Type `constants`)
- [MemberName](#MemberName `type`)
  - [#ctor(name,paramNames)](##ctor(name,paramNames) `constructor`)
  - [#ctor(name)](##ctor(name) `constructor`)
  - [Caption](#Caption `property`)
  - [Kind](#Kind `property`)
  - [Link](#Link `property`)
  - [Namespace](#Namespace `property`)
  - [TypeName](#TypeName `property`)
  - [CompareTo()](#CompareTo() `method`)
  - [GetParamTypes()](#GetParamTypes() `method`)
  - [ToReferenceLink(useShortName)](#ToReferenceLink(useShortName) `method`)
- [MemberUnit](#MemberUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [Comparer](#Comparer `property`)
  - [Kind](#Kind `property`)
  - [Link](#Link `property`)
  - [TypeName](#TypeName `property`)
  - [ComplementType(group)](#ComplementType(group) `method`)
  - [ToMarkdown()](#ToMarkdown() `method`)
- [MemberUnitComparer](#MemberUnitComparer `type`)
  - [Compare()](#Compare() `method`)
- [ParamUnit](#ParamUnit `type`)
  - [#ctor(element,paramType)](##ctor(element,paramType) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(elements,paramTypes,memberKind)](#ToMarkdown(elements,paramTypes,memberKind) `method`)
- [PermissionUnit](#PermissionUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(elements)](#ToMarkdown(elements) `method`)
- [Program](#Program `type`)
  - [Main(args)](#Main(args) `method`)
- [RemarksUnit](#RemarksUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(element)](#ToMarkdown(element) `method`)
- [ReturnsUnit](#ReturnsUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(element)](#ToMarkdown(element) `method`)
- [SeealsoUnit](#SeealsoUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(elements)](#ToMarkdown(elements) `method`)
- [SummaryUnit](#SummaryUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(element)](#ToMarkdown(element) `method`)
- [TableOfContents](#TableOfContents `type`)
  - [#ctor(memberUnits)](##ctor(memberUnits) `constructor`)
  - [Link](#Link `property`)
  - [ToMarkdown()](#ToMarkdown() `method`)
- [Test](#Test `type`)
  - [#ctor()](##ctor() `constructor`)
  - [TestBacktickInSummary()](#TestBacktickInSummary() `method`)
  - [TestGenericException()](#TestGenericException() `method`)
  - [TestGenericParameter\`\`2(expression)](#TestGenericParameter\`\`2(expression) `method`)
  - [TestGenericPermission()](#TestGenericPermission() `method`)
  - [TestGenericReference()](#TestGenericReference() `method`)
  - [TestParamWithoutDescription(p)](#TestParamWithoutDescription(p) `method`)
  - [TestSeeLangword()](#TestSeeLangword() `method`)
  - [TestSpaceAfterInlineElements\`\`1()](#TestSpaceAfterInlineElements\`\`1() `method`)
- [TestGenericType\`2](#TestGenericType\`2 `type`)
  - [TestGenericMethod\`\`2()](#TestGenericMethod\`\`2() `method`)
- [TypeparamUnit](#TypeparamUnit `type`)
  - [#ctor(element)](##ctor(element) `constructor`)
  - [ToMarkdown()](#ToMarkdown() `method`)
  - [ToMarkdown(elements)](#ToMarkdown(elements) `method`)

<a name='t-vsxmd-units-assemblyunit'></a>
## AssemblyUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Assembly unit.

<a name='m-vsxmd-units-assemblyunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [AssemblyUnit](#AssemblyUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The assembly XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `assembly`. |

<a name='m-vsxmd-units-assemblyunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='t-vsxmd-units-baseunit'></a>
## BaseUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

The base unit.

<a name='m-vsxmd-units-baseunit-#ctor-system-xml-linq-xelement,system-string-'></a>
### #ctor(element,elementName) `constructor`

##### Summary

Initializes a new instance of the [BaseUnit](#BaseUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The XML element. |
| elementName | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The expected XML element name. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML `element` name not matches the expected `elementName`. |

<a name='p-vsxmd-units-baseunit-element'></a>
### Element `property`

##### Summary

Gets the XML element.

<a name='p-vsxmd-units-baseunit-elementcontent'></a>
### ElementContent `property`

##### Summary

Gets the Markdown content representing the element.

<a name='m-vsxmd-units-baseunit-getattribute-system-xml-linq-xname-'></a>
### GetAttribute(name) `method`

##### Summary

Returns the [XAttribute](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XAttribute 'System.Xml.Linq.XAttribute') value of this [XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') that has the specified `name`.

##### Returns

An [XAttribute](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XAttribute 'System.Xml.Linq.XAttribute') value that has the specified `name`; `null` if there is no attribute with the specified `name`.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.Xml.Linq.XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') | The [XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') of the [XAttribute](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XAttribute 'System.Xml.Linq.XAttribute') to get. |

<a name='m-vsxmd-units-baseunit-getchild-system-xml-linq-xname-'></a>
### GetChild(name) `method`

##### Summary

Gets the first (in document order) child element with the specified `name`.

##### Returns

A [XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') that matches the specified `name`, or `null`.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.Xml.Linq.XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') | The [XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') to match. |

<a name='m-vsxmd-units-baseunit-getchildren-system-xml-linq-xname-'></a>
### GetChildren(name) `method`

##### Summary

Returns a collection of the child elements of this element or document, in document order.
Only elements that have a matching [XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') are included in the collection.

##### Returns

An [IEnumerable\`1](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable`1 'System.Collections.Generic.IEnumerable`1') of [XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') containing the children that have a matching [XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName'), in document order.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.Xml.Linq.XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') | The [XName](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XName 'System.Xml.Linq.XName') to match. |

<a name='m-vsxmd-units-baseunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='t-vsxmd-converter'></a>
## Converter `type`

##### Namespace

Vsxmd

##### Summary

*Inherit from parent.*

<a name='m-vsxmd-converter-#ctor-system-xml-linq-xdocument-'></a>
### #ctor(document) `constructor`

##### Summary

Initializes a new instance of the [Converter](#Converter `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| document | [System.Xml.Linq.XDocument](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XDocument 'System.Xml.Linq.XDocument') | The XML document. |

<a name='m-vsxmd-converter-tomarkdown-system-xml-linq-xdocument-'></a>
### ToMarkdown(document) `method`

##### Summary

Convert VS XML document to Markdown syntax.

##### Returns

The generated Markdown content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| document | [System.Xml.Linq.XDocument](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XDocument 'System.Xml.Linq.XDocument') | The XML document. |

<a name='m-vsxmd-converter-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='t-vsxmd-units-exampleunit'></a>
## ExampleUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Example unit.

<a name='m-vsxmd-units-exampleunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [ExampleUnit](#ExampleUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The example XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `example`. |

<a name='m-vsxmd-units-exampleunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-exampleunit-tomarkdown-system-xml-linq-xelement-'></a>
### ToMarkdown(element) `method`

##### Summary

Convert the example XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The example XML element. |

<a name='t-vsxmd-units-exceptionunit'></a>
## ExceptionUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Exception unit.

<a name='m-vsxmd-units-exceptionunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [ExceptionUnit](#ExceptionUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The exception XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `exception`. |

<a name='m-vsxmd-units-exceptionunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-exceptionunit-tomarkdown-system-collections-generic-ienumerable{system-xml-linq-xelement}-'></a>
### ToMarkdown(elements) `method`

##### Summary

Convert the exception XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | [System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}') | The exception XML element list. |

<a name='t-vsxmd-units-extensions'></a>
## Extensions `type`

##### Namespace

Vsxmd.Units

##### Summary

Extensions helper.

<a name='m-vsxmd-units-extensions-ascode-system-string-'></a>
### AsCode(code) `method`

##### Summary

Wrap the `code` into Markdown backtick safely.

The backtick characters inside the `code` reverse as it is.

##### Returns

The Markdown code span.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| code | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The code span. |

##### Remarks

Reference: http://meta.stackexchange.com/questions/55437/how-can-the-backtick-character-be-included-in-code .

<a name='m-vsxmd-units-extensions-escape-system-string-'></a>
### Escape(content) `method`

##### Summary

Escape the content to keep it raw in Markdown syntax.

##### Returns

The escaped content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| content | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The content. |

<a name='m-vsxmd-units-extensions-join-system-collections-generic-ienumerable{system-string},system-string-'></a>
### Join(value,separator) `method`

##### Summary

Concatenates the `value`s with the `separator`.

##### Returns

The concatenated string.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| value | [System.Collections.Generic.IEnumerable{System.String}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.String}') | The string values. |
| separator | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The separator. |

<a name='m-vsxmd-units-extensions-nthlast``1-system-collections-generic-ienumerable{``0},system-int32-'></a>
### NthLast\`\`1(source,index) `method`

##### Summary

Gets the n-th last element from the `source`.

##### Returns

The element at the specified position in the `source` sequence.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| source | [System.Collections.Generic.IEnumerable{\`\`0}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{``0}') | The source enumerable. |
| index | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The index for the n-th last. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| TSource | The type of the elements of `source`. |

<a name='m-vsxmd-units-extensions-suffix-system-string,system-string-'></a>
### Suffix(value,suffix) `method`

##### Summary

Suffix the `suffix` to the `value`, and generate a new string.

##### Returns

The new string.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| value | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The original string value. |
| suffix | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The suffix string. |

<a name='m-vsxmd-units-extensions-takeallbutlast``1-system-collections-generic-ienumerable{``0},system-int32-'></a>
### TakeAllButLast\`\`1(source,count) `method`

##### Summary

Take all element except the last `count`.

##### Returns

The generated enumerable.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| source | [System.Collections.Generic.IEnumerable{\`\`0}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{``0}') | The source enumerable. |
| count | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The number to except. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| TSource | The type of the elements of `source`. |

<a name='m-vsxmd-units-extensions-toanchor-system-string-'></a>
### ToAnchor(href) `method`

##### Summary

Generate an anchor for the `href`.

##### Returns

The anchor for the `href`.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| href | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The href. |

<a name='m-vsxmd-units-extensions-toherelink-system-string-'></a>
### ToHereLink(href) `method`

##### Summary

Generate "to here" link for the `href`.

##### Returns

The "to here" link for the `href`.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| href | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The href. |

<a name='m-vsxmd-units-extensions-tolowerstring-vsxmd-units-memberkind-'></a>
### ToLowerString(memberKind) `method`

##### Summary

Convert the [MemberKind](#MemberKind `type`) to its lowercase name.

##### Returns

The member kind's lowercase name.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| memberKind | [Vsxmd.Units.MemberKind](#MemberKind `type`) | The member kind. |

<a name='m-vsxmd-units-extensions-tomarkdowntext-system-xml-linq-xelement-'></a>
### ToMarkdownText(element) `method`

##### Summary

Convert the inline XML nodes to Markdown text.
For example, it works for `summary` and `returns` elements.

##### Returns

The generated Markdown content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The XML element. |

##### Example

This method converts the following `summary` element.

```
<summary>The <paramref name="element" /> value is <value>null</value>, it throws <c>ArgumentException</c>. For more, see <see cref="M:Vsxmd.Units.Extensions.ToMarkdownText(System.Xml.Linq.XElement)" />.</summary>
```

To the below Markdown content.

```
The `element` value is `null`, it throws `ArgumentException`. For more, see `ToMarkdownText`.
```

<a name='m-vsxmd-units-extensions-toreferencelink-system-string,system-boolean-'></a>
### ToReferenceLink(memberName,useShortName) `method`

##### Summary

Generate the reference link for the `memberName`.

##### Returns

The generated reference link.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| memberName | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The member name. |
| useShortName | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicate if use short type name. |

##### Example

For `T:Vsxmd.Units.MemberUnit`, convert it to `[MemberUnit](#T-Vsxmd.Units.MemberUnit)`.

For `T:System.ArgumentException`, convert it to `[ArgumentException](http://msdn/path/to/System.ArgumentException)`.

<a name='t-vsxmd-iconverter'></a>
## IConverter `type`

##### Namespace

Vsxmd

##### Summary

Converter for XML document to Markdown syntax conversion.

<a name='m-vsxmd-iconverter-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

Convert to Markdown syntax.

##### Returns

The generated Markdown content.

##### Parameters

This method has no parameters.

<a name='t-vsxmd-units-iunit'></a>
## IUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

[IUnit](#IUnit `type`) is wrapper to handle XML elements.

<a name='m-vsxmd-units-iunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

Represent the XML element content as Markdown syntax.

##### Returns

The generated Markdown content.

##### Parameters

This method has no parameters.

<a name='t-vsxmd-units-memberkind'></a>
## MemberKind `type`

##### Namespace

Vsxmd.Units

##### Summary

The member kind.

<a name='f-vsxmd-units-memberkind-constants'></a>
### Constants `constants`

##### Summary

Constants

<a name='f-vsxmd-units-memberkind-constructor'></a>
### Constructor `constants`

##### Summary

Constructor.

<a name='f-vsxmd-units-memberkind-method'></a>
### Method `constants`

##### Summary

Method.

<a name='f-vsxmd-units-memberkind-notsupported'></a>
### NotSupported `constants`

##### Summary

Not supported member kind.

<a name='f-vsxmd-units-memberkind-property'></a>
### Property `constants`

##### Summary

Property.

<a name='f-vsxmd-units-memberkind-type'></a>
### Type `constants`

##### Summary

Type.

<a name='t-vsxmd-units-membername'></a>
## MemberName `type`

##### Namespace

Vsxmd.Units

##### Summary

Member name.

<a name='m-vsxmd-units-membername-#ctor-system-string,system-collections-generic-ienumerable{system-string}-'></a>
### #ctor(name,paramNames) `constructor`

##### Summary

Initializes a new instance of the [MemberName](#MemberName `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The raw member name. For example, `T:Vsxmd.Units.MemberName`. |
| paramNames | [System.Collections.Generic.IEnumerable{System.String}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.String}') | The parameter names. It is only used when member kind is [Constructor](#Constructor `constants`) or [Method](#Method `constants`). |

<a name='m-vsxmd-units-membername-#ctor-system-string-'></a>
### #ctor(name) `constructor`

##### Summary

Initializes a new instance of the [MemberName](#MemberName `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The raw member name. For example, `T:Vsxmd.Units.MemberName`. |

<a name='p-vsxmd-units-membername-caption'></a>
### Caption `property`

##### Summary

Gets the caption representation for this member name.

##### Example

For [Type](#Type `constants`), show as `## Vsxmd.Units.MemberName [#](#here) [^](#contents)`.

For other kinds, show as `### Vsxmd.Units.MemberName.Caption [#](#here) [^](#contents)`.

<a name='p-vsxmd-units-membername-kind'></a>
### Kind `property`

##### Summary

Gets the member kind, one of [MemberKind](#MemberKind `type`).

<a name='p-vsxmd-units-membername-link'></a>
### Link `property`

##### Summary

Gets the link pointing to this member unit.

<a name='p-vsxmd-units-membername-namespace'></a>
### Namespace `property`

##### Summary

Gets the namespace name.

##### Example

`System`, `Vsxmd`, `Vsxmd.Units`.

<a name='p-vsxmd-units-membername-typename'></a>
### TypeName `property`

##### Summary

Gets the type name.

##### Example

`Vsxmd.Program`, `Vsxmd.Units.TypeUnit`.

<a name='m-vsxmd-units-membername-compareto-vsxmd-units-membername-'></a>
### CompareTo() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-membername-getparamtypes'></a>
### GetParamTypes() `method`

##### Summary

Gets the method parameter type names from the member name.

##### Returns

The method parameter type name list.

##### Parameters

This method has no parameters.

##### Example

It will prepend the type kind character (`T:`) to the type string.

For `(System.String,System.Int32)`, returns `["T:System.String","T:System.Int32"]`.

It also handle generic type.

For `(System.Collections.Generic.IEnumerable{System.String})`, returns `["T:System.Collections.Generic.IEnumerable{System.String}"]`.

<a name='m-vsxmd-units-membername-toreferencelink-system-boolean-'></a>
### ToReferenceLink(useShortName) `method`

##### Summary

Convert the member name to Markdown reference link.

If then name is under `System` namespace, the link points to MSDN.

Otherwise, the link points to this page anchor.

##### Returns

The generated Markdown reference link.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| useShortName | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicate if use short type name. |

<a name='t-vsxmd-units-memberunit'></a>
## MemberUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Member unit.

<a name='m-vsxmd-units-memberunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [MemberUnit](#MemberUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The member XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `member`. |

<a name='p-vsxmd-units-memberunit-comparer'></a>
### Comparer `property`

##### Summary

Gets the member unit comparer.

<a name='p-vsxmd-units-memberunit-kind'></a>
### Kind `property`

##### Summary

Gets the member kind, one of [MemberKind](#MemberKind `type`).

<a name='p-vsxmd-units-memberunit-link'></a>
### Link `property`

##### Summary

Gets the link pointing to this member unit.

<a name='p-vsxmd-units-memberunit-typename'></a>
### TypeName `property`

##### Summary

Gets the type name.

##### Example

`Vsxmd.Program`, `Vsxmd.Units.TypeUnit`.

<a name='m-vsxmd-units-memberunit-complementtype-system-collections-generic-ienumerable{vsxmd-units-memberunit}-'></a>
### ComplementType(group) `method`

##### Summary

Complement a type unit if the member unit `group` does not have one.
One member unit group has the same [TypeName](#TypeName `property`).

##### Returns

The complemented member unit group.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| group | [System.Collections.Generic.IEnumerable{Vsxmd.Units.MemberUnit}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{Vsxmd.Units.MemberUnit}') | The member unit group. |

<a name='m-vsxmd-units-memberunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='t-vsxmd-units-memberunit-memberunitcomparer'></a>
## MemberUnitComparer `type`

##### Namespace

Vsxmd.Units.MemberUnit

<a name='m-vsxmd-units-memberunit-memberunitcomparer-compare-vsxmd-units-memberunit,vsxmd-units-memberunit-'></a>
### Compare() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='t-vsxmd-units-paramunit'></a>
## ParamUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Param unit.

<a name='m-vsxmd-units-paramunit-#ctor-system-xml-linq-xelement,system-string-'></a>
### #ctor(element,paramType) `constructor`

##### Summary

Initializes a new instance of the [ParamUnit](#ParamUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The param XML element. |
| paramType | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The parameter type corresponding to the param XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `param`. |

<a name='m-vsxmd-units-paramunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-paramunit-tomarkdown-system-collections-generic-ienumerable{system-xml-linq-xelement},system-collections-generic-ienumerable{system-string},vsxmd-units-memberkind-'></a>
### ToMarkdown(elements,paramTypes,memberKind) `method`

##### Summary

Convert the param XML element to Markdown safely.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | [System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}') | The param XML element list. |
| paramTypes | [System.Collections.Generic.IEnumerable{System.String}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.String}') | The paramater type names. |
| memberKind | [Vsxmd.Units.MemberKind](#MemberKind `type`) | The member kind of the parent element. |

##### Remarks

When the parameter (a.k.a `elements`) list is empty:

If parent element kind is [Constructor](#Constructor `constants`) or [Method](#Method `constants`), it returns a hint about "no parameters".

If parent element kind is not the value mentioned above, it returns an empty string.

<a name='t-vsxmd-units-permissionunit'></a>
## PermissionUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Permission unit.

<a name='m-vsxmd-units-permissionunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [PermissionUnit](#PermissionUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The permission XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `permission`. |

<a name='m-vsxmd-units-permissionunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-permissionunit-tomarkdown-system-collections-generic-ienumerable{system-xml-linq-xelement}-'></a>
### ToMarkdown(elements) `method`

##### Summary

Convert the permission XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | [System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}') | The permission XML element list. |

<a name='t-vsxmd-program'></a>
## Program `type`

##### Namespace

Vsxmd

##### Summary

Program entry.

##### Remarks

Usage syntax:

```
Vsxmd.exe &lt;input-XML-path&gt; [output-Markdown-path]
```

The `input-XML-path` argument is required. It references to the VS generated XML documentation file.

The `output-Markdown-path` argument is optional. It indicates the file path for the Markdown output file. When not specific, it will be a `.md` file with same file name as the XML documentation file, path at the XML documentation folder.

<a name='m-vsxmd-program-main-system-string[]-'></a>
### Main(args) `method`

##### Summary

Program main function entry.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| args | [System.String[]](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String[] 'System.String[]') | Program arguments. |

##### See Also

- [Vsxmd.Program](#Program `type`)

<a name='t-vsxmd-units-remarksunit'></a>
## RemarksUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Remarks unit.

<a name='m-vsxmd-units-remarksunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [RemarksUnit](#RemarksUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The remarks XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `remarks`. |

<a name='m-vsxmd-units-remarksunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-remarksunit-tomarkdown-system-xml-linq-xelement-'></a>
### ToMarkdown(element) `method`

##### Summary

Convert the remarks XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The remarks XML element. |

<a name='t-vsxmd-units-returnsunit'></a>
## ReturnsUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Returns unit.

<a name='m-vsxmd-units-returnsunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [ReturnsUnit](#ReturnsUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The returns XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `returns`. |

<a name='m-vsxmd-units-returnsunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-returnsunit-tomarkdown-system-xml-linq-xelement-'></a>
### ToMarkdown(element) `method`

##### Summary

Convert the returns XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The returns XML element. |

<a name='t-vsxmd-units-seealsounit'></a>
## SeealsoUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Seealso unit.

<a name='m-vsxmd-units-seealsounit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [SeealsoUnit](#SeealsoUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The seealso XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `seealso`. |

<a name='m-vsxmd-units-seealsounit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-seealsounit-tomarkdown-system-collections-generic-ienumerable{system-xml-linq-xelement}-'></a>
### ToMarkdown(elements) `method`

##### Summary

Convert the seealso XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | [System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}') | The seealso XML element list. |

<a name='t-vsxmd-units-summaryunit'></a>
## SummaryUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Summary unit.

<a name='m-vsxmd-units-summaryunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [SummaryUnit](#SummaryUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The summary XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `summary`. |

<a name='m-vsxmd-units-summaryunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-summaryunit-tomarkdown-system-xml-linq-xelement-'></a>
### ToMarkdown(element) `method`

##### Summary

Convert the summary XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The summary XML element. |

<a name='t-vsxmd-tableofcontents'></a>
## TableOfContents `type`

##### Namespace

Vsxmd

##### Summary

Table of contents.

<a name='m-vsxmd-tableofcontents-#ctor-system-linq-iorderedenumerable{vsxmd-units-memberunit}-'></a>
### #ctor(memberUnits) `constructor`

##### Summary

Initializes a new instance of the [TableOfContents](#TableOfContents `type`) class.

It convert the table of contents from the `memberUnits`.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| memberUnits | [System.Linq.IOrderedEnumerable{Vsxmd.Units.MemberUnit}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Linq.IOrderedEnumerable 'System.Linq.IOrderedEnumerable{Vsxmd.Units.MemberUnit}') | The member unit list. |

<a name='p-vsxmd-tableofcontents-link'></a>
### Link `property`

##### Summary

Gets the link pointing to the table of contents.

<a name='m-vsxmd-tableofcontents-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

Convert the table of contents to Markdown syntax.

##### Returns

The table of contents in Markdown syntax.

##### Parameters

This method has no parameters.

<a name='t-vsxmd-program-test'></a>
## Test `type`

##### Namespace

Vsxmd.Program

<a name='m-vsxmd-program-test-#ctor'></a>
### #ctor() `constructor`

##### Summary

Initializes a new instance of the [Test](#Test `type`) class.

Test constructor without parameters.

See [Test.#ctor](##ctor() `constructor`).

##### Parameters

This constructor has no parameters.

##### Permissions

| Name | Description |
| ---- | ----------- |
| [Vsxmd.Program](#Program `type`) | Just for test. |

<a name='m-vsxmd-program-test-testbacktickinsummary'></a>
### TestBacktickInSummary() `method`

##### Summary

Test backtick characters in summary comment.

See \`should not inside code block\`.

See `` `backtick inside code block` ``.

See \``code block inside backtick`\`.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

<a name='m-vsxmd-program-test-testgenericexception'></a>
### TestGenericException() `method`

##### Summary

Test generic exception type.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [Vsxmd.Program.Test.TestGenericParameter\`\`2](#TestGenericParameter\`\`2() `method`) | Just for test. |

<a name='m-vsxmd-program-test-testgenericparameter``2-system-linq-expressions-expression{system-func{``0,``1,system-string}}-'></a>
### TestGenericParameter\`\`2(expression) `method`

##### Summary

Test generic parameter type.

See `T1` and `T2`.

##### Returns

Nothing.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| expression | [System.Linq.Expressions.Expression{System.Func{\`\`0,\`\`1,System.String}}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Linq.Expressions.Expression 'System.Linq.Expressions.Expression{System.Func{``0,``1,System.String}}') | The linq expression. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| T1 | Generic type 1. |
| T2 | Generic type 2. |

<a name='m-vsxmd-program-test-testgenericpermission'></a>
### TestGenericPermission() `method`

##### Summary

Test generic exception type.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

##### Permissions

| Name | Description |
| ---- | ----------- |
| [Vsxmd.Program.Test.TestGenericParameter\`\`2](#TestGenericParameter\`\`2() `method`) | Just for test. |

<a name='m-vsxmd-program-test-testgenericreference'></a>
### TestGenericReference() `method`

##### Summary

Test generic reference type.

See [TestGenericParameter\`\`2](#TestGenericParameter\`\`2() `method`).

##### Returns

Nothing.

##### Parameters

This method has no parameters.

<a name='m-vsxmd-program-test-testparamwithoutdescription-system-string-'></a>
### TestParamWithoutDescription(p) `method`

##### Summary

Test a param tag without description.

##### Returns

Nothing.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| p | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') |  |

<a name='m-vsxmd-program-test-testseelangword'></a>
### TestSeeLangword() `method`

##### Summary

Test see tag with langword attribute. See `true`.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

<a name='m-vsxmd-program-test-testspaceafterinlineelements``1-system-boolean-'></a>
### TestSpaceAfterInlineElements\`\`1() `method`

##### Summary

Test space after inline elements.

See `code block` should follow a space.

See a value at the end of a `sentence`.

See [TestSpaceAfterInlineElements\`\`1](#TestSpaceAfterInlineElements\`\`1() `method`) as a link.

See `space` after a param ref.

See `T` after a type param ref.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

<a name='t-vsxmd-program-testgenerictype`2'></a>
## TestGenericType\`2 `type`

##### Namespace

Vsxmd.Program

##### Summary

Test generic type.

See [TestGenericType\`2](#TestGenericType\`2 `type`).

##### Generic Types

| Name | Description |
| ---- | ----------- |
| T1 | Generic type 1. |
| T2 | Generic type 2. |

<a name='m-vsxmd-program-testgenerictype`2-testgenericmethod``2'></a>
### TestGenericMethod\`\`2() `method`

##### Summary

Test generic method.

See [TestGenericMethod\`\`2](#TestGenericMethod\`\`2() `method`).

##### Returns

Nothing.

##### Parameters

This method has no parameters.

##### Generic Types

| Name | Description |
| ---- | ----------- |
| T3 | Generic type 3. |
| T4 | Generic type 4. |

<a name='t-vsxmd-units-typeparamunit'></a>
## TypeparamUnit `type`

##### Namespace

Vsxmd.Units

##### Summary

Typeparam unit.

<a name='m-vsxmd-units-typeparamunit-#ctor-system-xml-linq-xelement-'></a>
### #ctor(element) `constructor`

##### Summary

Initializes a new instance of the [TypeparamUnit](#TypeparamUnit `type`) class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | [System.Xml.Linq.XElement](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Xml.Linq.XElement 'System.Xml.Linq.XElement') | The typeparam XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| [System.ArgumentException](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ArgumentException 'System.ArgumentException') | Throw if XML element name is not `typeparam`. |

<a name='m-vsxmd-units-typeparamunit-tomarkdown'></a>
### ToMarkdown() `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

<a name='m-vsxmd-units-typeparamunit-tomarkdown-system-collections-generic-ienumerable{system-xml-linq-xelement}-'></a>
### ToMarkdown(elements) `method`

##### Summary

Convert the param XML element to Markdown safely.
If element is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | [System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable 'System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement}') | The param XML element list. |
