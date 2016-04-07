---
inFeed: true
hasPage: true
inNav: false
inLanguage: null
starred: false
keywords: []
description: 'One criticism that has been thrown against the Ruby language is the do syntax, as opposed to simply using higher-order functions in any parameter position.'
datePublished: '2016-04-07T09:56:05.342Z'
dateModified: '2016-04-07T09:55:57.635Z'
title: ''
author: []
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
sourcePath: _posts/2016-04-07-one-criticism-that-has-been-thrown-against-the-ruby-language.md
published: true
url: one-criticism-that-has-been-thrown-against-the-ruby-language/index.html
_type: Article

---
One criticism that has been thrown against the Ruby language is the do syntax, as opposed to simply using higher-order functions in any parameter position.

Ruby's do basically comes down to a higher-order function that is always in a special position in the function definition syntax. In other languages the emphasis on orthogonality, where you can pass a function to another function in any parameter position.

If one looks at Haskell or Javascript, one finds that basically all HOF's take one other function as a parameter. In Haskell this HOF is usually in the first parameter position, in order to enable currying. In Javascript, function parameters are usually callbacks, and to enable callback hell the HOF is in the last parameter position (_setTimeout_ being a notable, and irritating, exception).

Considering that basically all HOF take only one function parameter in any case Ruby's do syntax seems like a good compromise. The syntax is certainly easier to read than Javascript's multiple function(function(function boilerplates, although ES6's arrow syntax now mitigates this to some extent. 

It should be noted that Ruby _does_ allow arbitary functions in different position, if one passes them as Procs, and then the syntax is not much different from pre-ES6 Javascript. 

The do-block also makes for many useful and wonderful DSL's and goes a long way towards mitigating LISP/Clojure's need for macros. Elixir, a pure functional language, also took over the do syntax for function parameters.

All in all, the do syntax is a good compromise between clarity, the trickiness of full LISP macros and the orthogonality but clumsy syntax of Javascript/Python.