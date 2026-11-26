# Exercise 06 – Box Model and Display

## Content-box vs Border-box

### Content-box

In `content-box`, the specified width only includes the content. Padding and border are added to calculate the total width.

**Formula:**

Total width = width + left/right padding + left/right border

### Border-box

In `border-box`, the specified width already includes the content, padding, and border.

**Formula:**

Total width = specified width

The content width is calculated by subtracting padding and border from the specified width.

### Width Predictions

| Box | Content-box | Border-box |
|---|---|---|
| Outer | 350px | 300px |
| Middle | 216px | 180px |
| Inner | 104px | 80px |

Margins are not included in these widths. They create additional space outside the border.

The main difference is that `content-box` adds padding and border to the specified width, while `border-box` includes them. This makes `border-box` easier to use when controlling element sizes.

## Margin Collapsing

Margin collapsing happens when vertical margins of block elements in normal flow overlap under certain conditions.

For example, if one paragraph has `margin-bottom: 50px` and the next paragraph has `margin-top: 30px`, the resulting gap is 50px, not 80px.

This happens because the two positive margins collapse, and the larger margin determines the space between the elements.

Horizontal margins do not collapse.

## DevTools Results

all my predictions were correct