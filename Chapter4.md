## Chapter 4
### Ways to utilize CSS
- style tags: `<style>[insert CSS Code]</style>`
    - Makes html much too long
- style attribute `<[element] style="[]">`
    - invites inconsistency by forcing manual repetition for each element
    - not good programming practice
- style page: `<link rel="stylesheet" href="styles.css">`
    - link tag in `<head>` section of webpage
### Syntax
```
[selector] {
    property: value;
}
```
**Type Selector**
- element
- id `#`
- class  `.`
**Universal Selector**
- wildcard `*` 
**Colors**
- rgba: 
    - a = alpha value = transparency 
    - between 0 and 1
- rgb
- hsl: Hexadecimal
- choose easy to read colors (light on dark or dark on light)
Fonts
- font-weight: boldness
- font-family: 
- line-height: vertical space between each line
    - can use variety of units of measurements
- font-size:
- text-indent: indents first line in paragraph
- alternative syntax:
    - `font: [property], [property], etc.`
- text-shadow: 
    - `<[horizontal offset] [vertical offset] [blur radius] [shadow colors]>`
    - ex: `textshadow: 5px 5px 5px #675937`
**Percentages in CSS**
- rem: Relative to root `(<html>)` element's font size 
    - default is normally 16px; 1 rem = 16px
- em: Relative to font size of element or its parent
- percentage: Relative to parent element's matching property
- pixels: fixed unit; doesn't scale with user settings
    - to be avoided in this class
**Spacing**
- float: pushes element to left or right
    - text and inline content wrap
- margin: space outside element's border
    - `margin: [top %] [right %] [right %] [bottom %] [left %]`
    - `margin: 0 auto`: centers block element horizontally
- clear: stops element from being next to floating element
    - values: left, right, both, none
**Relational Selectors**
- `[parent tag]>[child tag]`: selects all children that belong to parent
- `[sibling tag]~[sibling tag]`: same indentation
- `[element tag] [element tag]`: indentation
- `[adjacent sibling tag]+[adjacent sibling tag]`: 
**Combination Selectors**
- `[element tag]:[class]`: selector for class within an element
- `[selector], [selector], [selector], etc.`: selects multiple selectors
**Attribute Selectors - utilize `[]`**
- `*[attribute]` - any tag with the attribute
- `(tag)[attribute]]`
**Pseudo-classes** 
- `:link` - hasn't been visited
- `:visited` - link has been visited
- `:active` - mouse button clicked but not released
- :hover - mouse hovering over
- :focus - element that has focus
    - ex: mouse on particular part of a form
- child pseudo-classes
    - `:first-child`
    - `:last-child`
    - `:only-child`
**Pseudo-elements**
- `::first-letter` - first letter of an element
- `::first-line` - last letter of an element
### Cascade Rules
1. Style rule with the highest specificity will will
2. If same specificity, the last style rule applied wins
- If multiple styles sheets, the last one will override
- User style sheets: users can create special styles for their browsers
    - ex: people with difficulty seeing fonts can enlarge fonts
- Improve precedence of style rule with `!important` at the end
- use `:hov` in developer view to debug 
**Custom Properties**
- aka variables
- declared with `:[selector] {--(variable name):(variable)}`
- `:root` sets up variables for `<html>` element


