
## `<abbr>`

The ``<abbr>`` tag is used to define abbreviations or acronyms, providing a tooltip with the full meaning when hovered over. It improves accessibility and semantic HTML.

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

### use aria for better Accessibility
```js
aria-label="HyperText Markup Language"
aria-describedby="desc"
```

```html
<p>
  The <abbr id="html" title="HyperText Markup Language" aria-describedby="desc">HTML</abbr> standard is evolving.
</p>
<p id="desc">A widely used markup language for web pages.</p>
```