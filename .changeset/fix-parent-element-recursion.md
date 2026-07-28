---
"click-to-react-component": patch
---

Fix infinite recursion in `getFirstParentElementWithSource` that caused "Maximum call stack size exceeded". The recursive call passed the original `element` instead of `parentElement`, so it never walked up the DOM tree when a parent had no source.
