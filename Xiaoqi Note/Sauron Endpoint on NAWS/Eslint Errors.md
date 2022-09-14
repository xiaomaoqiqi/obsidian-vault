---
created: 2022-09-09T15:44:06-04:00
updated: 2022-09-09T15:45:52-04:00
---
 Eslint documentation:
 https://eslint.org/docs/latest/rules/no-unused-vars
 
 
 
 
 
 Eslint error  'pipeline' is assigned a value but never used  no-unused-vars


This is an eslint rule [http://eslint.org/docs/rules/no-unused-vars](http://eslint.org/docs/rules/no-unused-vars). It prevents you from creating variables that you never use, which causes code clutter or could mean you're using variables that aren't what you think they are.

If you're using a poorly designed library where the class constructor has side effects (which it isn't supposed to), and you don't need to do anything with the returned value from the class, I would disable that specific eslint rule for the create line with [eslint disable comments](https://eslint.org/docs/2.13.1/user-guide/configuring#disabling-rules-with-inline-comments-1):

```javascript
// eslint-disable-next-line no-unused-vars
const modal = new VanillaModal({
  modal: '.c-modal',
  modalInner: '.js-modal__inner',
  modalContent: '.js-modal__content',
  open: '[rel="js-modal:open"]',
  close: '[rel="js-modal:close"]',
  class: 'js-modal--visible',
  loadClass: 'js-modal--loaded',
});
```

You can also wrap any block of code with eslint specific comments to disable a rule for that block:

```javascript
/* eslint-disable no-unused-vars */
const modal = new VanillaModal({
    ...
});
/* eslint-enable no-unused-vars */
```

