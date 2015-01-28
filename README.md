# url-parser
Mostly code from Crossroads.js (thanks!) to extract the "matching of url pattern" (Pattern Lexer) part.

##Examples (taken from the Crossroads.js website)

###String rule with param: '/news/{id}'
match '/news/123' passing "123" as param to handler

###String rule with optional param: '/foo/{id}/:slug:'
match '/foo/123/bar' passing "123" and "bar" as param
match '/foo/45' passing 45 as param (slug is optional)

###RegExp rule: /^\/lorem\/([a-z]+)$/
match '/lorem/ipsum' passing "ipsum" as param to handler
note the capturing group around segment

###String rule with rest segments: '/foo/{id*}/edit'
match '/foo/123/edit' passing "123" as argument
match '/foo/45/asd/123/edit' passing "45/asd/123" as argument

###Query String: 'foo.php{?query}'
match 'foo.php?lorem=ipsum&dolor=amet'