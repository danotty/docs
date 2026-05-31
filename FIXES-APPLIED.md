# Fixes Applied to Documentation

## Date: May 31, 2026

## Issue: MDX Parsing Error

### Error Message
```
parsing error .\signals\signal-scoring.mdx:25:20 - Unexpected character `4` (U+0034) before name, expected a character that can start a name, such as a letter, `$`, or `_`
```

### Root Cause
Line 25 in `signals/signal-scoring.mdx` contained `<40` which MDX was trying to parse as an HTML tag opening. The `<` character needs to be escaped in MDX when used in text content.

### Fix Applied
Changed `<40` to `&lt;40` (HTML entity for less-than symbol)

**Before:**
```markdown
- **Low Priority (<40):** Filtered out of standard views to reduce noise.
```

**After:**
```markdown
- **Low Priority (&lt;40):** Filtered out of standard views to reduce noise.
```

### Verification
- ✅ File exists at correct path
- ✅ No other unescaped `<` or `>` characters found in MDX files
- ✅ Ready for local preview with `mintlify dev`

## Common MDX Gotchas to Avoid

When editing MDX files, remember to escape these characters in text:
- `<` → `&lt;`
- `>` → `&gt;`
- `&` → `&amp;`

Or use code blocks/inline code for technical content with these characters.
