# Client-side full-text search in CSS
Using data- attributes for indexation, and a dynamic stylesheet with a CSS3 selector for search, it is straightforward to implement a client-side full-text search in CSS rather than JavaScript. Here is an example.  

## The Search Code
The search is very straightforward: it relies on two well-supported CSS3 selectors (':not()' and '[attr*=]') and the rewriting of a style rule each time the search input is modified:  

The advantage of using CSS selectors rather than JavaScript 'indexOf()' for search is speed: you only change one element at each keystroke (the '<style>' tag) instead of changing all the elements matching the query. Using the ':not()' selector, this implementation works on IE9+, but it could easily be made compatible with IE8+ by using two rules instead of one.