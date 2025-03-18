---
layout: default
title: UI Components
nav_order: 3
has_children: false
permalink: /docs/ui-components
---

# UI Components
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Buttons

Buttons are styled links that can be used for primary actions or navigation.

### Basic Button

```html
[Get Started](#getting-started){: .btn }
```

### Button Types

- Primary Button: `{: .btn .btn-primary }`
- Purple Button: `{: .btn .btn-purple }`
- Blue Button: `{: .btn .btn-blue }`
- Green Button: `{: .btn .btn-green }`

### Button Sizes

- Small: `{: .btn .btn-sm }`
- Large: `{: .btn .btn-lg }`

## Labels

Labels are useful for adding context to items or highlighting status.

```html
Default label
{: .label }

Blue label
{: .label .label-blue }

Green label
{: .label .label-green }

Purple label
{: .label .label-purple }

Red label
{: .label .label-red }

Yellow label
{: .label .label-yellow }
```

## Typography

### Text Formatting

```markdown
*This text is italicized*
**This text is bold**
***This text is bold and italicized***
```

### Text Alignment

```markdown
This is left-aligned text
{: .text-left }

This is center-aligned text
{: .text-center }

This is right-aligned text
{: .text-right }
```

## Tables

### Basic Table

```markdown
| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |
{: .table }
```

### Responsive Table

```markdown
| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |
{: .table-responsive }
```

## Code Blocks

### Basic Code Block

```markdown
```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
```
```

### Code Block with Line Numbers

```markdown
```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
{: .line-numbers }
```
```

## Lists

### Unordered Lists

```markdown
- Item 1
- Item 2
  - Sub-item 1
  - Sub-item 2
```

### Ordered Lists

```markdown
1. First item
2. Second item
   1. Sub-item 1
   2. Sub-item 2
```

## Callouts

```markdown
{: .note }
A note callout

{: .warning }
A warning callout

{: .important }
An important callout
``` 