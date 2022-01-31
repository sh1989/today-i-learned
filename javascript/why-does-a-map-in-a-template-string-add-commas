# Why Does a Map in a Template String Add Commas?

This is one of those "oh, of course it does that" moments. Those used to JSX syntax may be quite familiar with the following looping construct:

```jsx
<ul>
  { items.map(i => <li>i</li>) }
</ul>
```

With the addition and widespread support of template strings in the JavaScript language, a very similar pattern can emerge:

```javascript
`<ul>
  ${items.map(i => `<li>${i}</li>`))}
<ul>`
```

However, this produces the following output, when `items = [1,2,3]`:

```
<ul>
  <li>1</li>,
  <li>2</li>,
  <li>3</li>
</ul>
```

Why is this? It's because `items` is an array, so it's outputted to a string via `join`, whose default separator is a `,`!
Fix with a manual call to `.join('\n')`, specifying a newline separator.
