## Details

If no elements in the graph match the selector, an empty [collection](#collection) is returned.

The function `cy.$()` acts as an alias to `cy.filter()`:  It lets you type less characters.  It is analogous to the jQuery `$` alias used to search the document

## Examples

Get nodes with weight greater than 50:
```js
cy.nodes('[weight > 50]');
```

Get edges with source node `n0`:
```js
cy.edges('[source = "j"]');
```

Get all nodes and edges with weight greater than 50:
```js
cy.elements('[weight > 50]');
cy.filter('[weight > 50]'); // works the same as the above line
```

Get nodes with weight greater than 50 with a filter function:
```js
cy.filter(function(element, i){
  return element.isNode() && element.data('weight') > 50;
});
```
