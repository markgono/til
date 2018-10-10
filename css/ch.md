# The CH Unit

The ch unit is based on the width of the `0` character in the currently applied `font-family` when used on an element. That's it!

## Use Case

```
<p>Hello world<span style="margin-left:1ch;">&#128170;</span></p>
```

It's extremley useful for margins between text and inline elements — like a one character gap between a text element and an svg glyph, for example.