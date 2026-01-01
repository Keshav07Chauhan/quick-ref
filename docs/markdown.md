> **Source & credit** 
>  
> This Markdown cheat sheet is based on the public reference at  
> https://quickref.me/markdown.

---
# Markdown Cheat Sheet


## Headers (ATX style)

```md
# h1
## h2
### h3
#### h4
##### h5
###### h6
````

## Headers (Setext style)

```md
Header 1
========

Header 2
--------
```

---

## Blockquotes

```md
> This is
> a blockquote
>
> > Nested
> > blockquote
```

---

## Unordered Lists

```md
* Item 1
* Item 2
  * Item 3a
  * Item 3b
```

Alternative markers:

```md
- Item 1
- Item 2
```

```md
+ Item 1
+ Item 2
```

Checkboxes:

```md
- [ ] Checkbox off
- [x] Checkbox on
```

---

## Ordered Lists

```md
1. Item 1
2. Item 2
   a. Item 3a
   b. Item 3b
```

---

## Links

Inline:

```md
[link](http://google.com)
```

Reference style:

```md
[link][google]

[google]: http://google.com
```

Automatic:

```md
<http://google.com>
```

---

## Emphasis

```md
*italic*
_italic_

**bold**
__bold__

`inline code`
~~strikethrough~~
```

---

## Horizontal Rules

Hyphens:

```md
---
```

Asterisks:

```md
***
```

Underscores:

```md
___
```

---

## Code Blocks

Fenced (recommended):

````md
```javascript
console.log("This is a block of code");
```
````


Alternative fencing:

````md
~~~css
.button {
  border: none;
}
~~~
````


Indented (not recommended)❌:

```md
    4 spaces make a code block
```

### Inline Code

```md
`inline code`
```

---

## Tables

Standard table:

```md
| Left column | Center column | Right column |
|:------------|:-------------:|-------------:|
| Cell 1      |   Centered    |        $1600 |
| Cell 2      |    Cell 3     |          $12 |
```

Simple style:

```md
Left column | Center column | Right column
:----------:|:-------------:|:-----------:
   Cell 1   |   Centered    |    $1600
   Cell 2   |    Cell 3     |     $12
```

---

## Images

Basic image:

```md
![Alt text](url)
```

With link:

```md
[![Alt text](image_url)](link_url)
```

Reference style:

```md
![alt text][logo]

[logo]: /images/logo.png "Logo Title"
```

---

## Backslash Escapes

| Character | Escape | Description     |
| --------: | :----: | --------------- |
|         \ |    \   | Backslash       |
|         ` |    `   | Backtick        |
|         * |    *   | Asterisk        |
|         _ |    _   | Underscore      |
|        {} |   {}   | Curly braces    |
|        [] |   []   | Square brackets |
|        () |   ()   | Parentheses     |
|         # |    #   | Hash            |
|         + |    +   | Plus            |
|         - |    -   | Minus           |
|         . |    .   | Dot             |
|         ! |    !   | Exclamation     |

---

## Notes

* Prefer fenced code blocks over indentation
* Avoid Setext headers in real projects
* Tables and task lists are **not part of original Markdown** but widely supported

---