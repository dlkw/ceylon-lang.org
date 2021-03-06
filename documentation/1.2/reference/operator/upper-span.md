---
layout: reference12
title_md: '`x[y...]` (upper span) operator'
tab: documentation
unique_id: docspage
author: Tom Bentley
doc_root: ../../..
---

# #{page.title_md}

The *upper span* operator returns the tail of its left-hand `Ranged` operand
as specified by its right-hand operand.

## Usage 

<!-- try: -->
    String[] names = {"foo", "bar", "baz"};
    String[] secondAndThird = names[1...];
    String[] third = names[2...];
    String[] emptySequence = names[3...];

## Description

### Definition

The `lhs[rhs...]` operator is defined as follows:

<!-- check:none -->
<!-- try: -->
    lhs.spanFrom(rhs)

See the [language specification](#{site.urls.spec_current}#listmap) for 
more details.

### Polymorphism

The `x[y...]` operator is [polymorphic](#{page.doc_root}/reference/operator/operator-polymorphism). 
The meaning of `x[y...]` depends on the 
[`Ranged`](#{site.urls.apidoc_1_2}/Ranged.type.html) 
interface.

### Type

The result type of the `lhs[from..]` operator is the element type of the `Ranged` `lhs`.

## See also

* [`x[y..z]` (span)](../span) operator used for obtaining a span of a `Ranged`.
* [`x[...z]` (lower span)](../lower-span) operator used for obtaining a span of a `Ranged`.
* API documentation for [`Ranged`](#{site.urls.apidoc_1_2}/Ranged.type.html)
* [sequence operators](#{site.urls.spec_current}#listmap) in the 
  language specification
* [operator precedence](#{site.urls.spec_current}#operatorprecedence) in the 
  language specification
* [Operator polymorphism](#{page.doc_root}/tour/language-module/#operator_polymorphism) 
  in the Tour of Ceylon

