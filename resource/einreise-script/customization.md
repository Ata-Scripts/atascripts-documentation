# Customization

### Customization

#### UI Text (html/local.js)

Edit the `languages` object in `html/local.js` to change UI text:

```javascript
var languages = {
  en: {
    enter: "ENTER",
    legal: "LEGAL",
    joinButton: "JOIN",
    illegal: "ILLEGAL",
    // Other text strings...
  },
  // Add other languages if needed
};
```

#### Questions

Edit questions in:

* `legal_question.lua` - Questions for legal path
* `illegal_question.lua` - Questions for illegal path

Question format:

```lua
{
    question = "What is example question?",
    a = "Answer option A",
    b = "Answer option B",
    c = "Answer option C",
    correct = "b"  -- Correct answer (a, b, or c)
}
```
