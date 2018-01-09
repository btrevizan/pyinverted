# pyinverted's API

`class` pyinverted.**Inverted**(*filename, n*): return a Inverted object.

- `string` **filename**: the filename/filepath without extension.
- `int` **n**: values' list length *(default 601)*.

### Methods
**insert**(*key, value*): insert a `value` for a `key`. If `key` does not exist, create it and set the `value`.

---
`list` **get**(*key*): get all values associated with a `key`.

---
**update**(*old, new*): change `old` key to `new` key.

---
**delete**(*key, value*): delete a `value` from a `key`.
