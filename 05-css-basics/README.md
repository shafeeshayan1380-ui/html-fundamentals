## DevTools Results

I checked all five CSS conflicts in Chrome DevTools, and all my predictions were correct.

## What I Learned About Specificity

I learned that CSS specificity determines which rule wins when multiple rules target the same element and property.

The more specific a selector is, the higher its priority.

There are different types of selectors with different specificity levels:

1. **Element selectors** (`p`, `h1`, `div`) — Specificity: `0-0-1`
2. **Class selectors** (`.intro`, `.nav-link`) — Specificity: `0-1-0`
3. **Pseudo-classes** (`:hover`, `:first-child`) — Specificity: `0-1-0`
4. **ID selectors** (`#about`, `#skills`) — Specificity: `1-0-0`

Inline styles have even higher priority than normal ID selector rules.

When selectors are combined, their specificity is calculated together. For example:

- `p` → `0-0-1`
- `.intro` → `0-1-0`
- `nav a` → `0-0-2`
- `section > h2` → `0-0-2`
- `.skills li:first-child` → `0-2-1`

If two competing rules have the same specificity and other cascade conditions are equal, the rule written later wins.

I also learned that `!important` can override normal declarations, but it is better to avoid using it unnecessarily because it makes CSS harder and messy to maintain.

## My Mistakes

I did not make any incorrect predictions. All five results matched my expectations after checking them in DevTools.