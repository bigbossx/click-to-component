---
"click-to-react-component": patch
---

Guard `getSourceForInstance` against an undefined instance. `getReactInstanceForElement` can return `undefined`, and destructuring `_debugSource` directly off it threw `Cannot destructure property '_debugSource' of 'undefined'`. Now returns early when there is no instance.
