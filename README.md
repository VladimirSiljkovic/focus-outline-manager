# focus-outline-manager

> Watch users keyboard input and manage the focus outline visibility

[![NPM version](https://badge.fury.io/js/focus-outline-manager.svg)](https://www.npmjs.com/package/focus-outline-manager)

> **NOTICE:** This library is no longer needed in most cases. Modern browsers added this behavior by default for most focusable elements, except for text `<input>` and `<textarea>`, for which you can show a custom focus indicator, such as a different outline or box-shadow. For example: `input:focus-visible, textarea:focus-visible { outline: 2px solid black; }`. Keep in mind that the custom focus indicator needs to be accessible (Minimum Contrast, Use of Color, etc). Unfortunatelly, for now, it is [not possible](https://stackoverflow.com/questions/70168063/styling-input-field-focused-by-keyboard) to set different styling on an input field which is focused by keyboard (not mouse) with CSS only, without JS. In case you want to change the default focus indicator style for all elements, without affecting the focus indicator visibility, you can use the new pseudo-class `:focus-visible` instead of `:focus`. For example: `:focus-visible {outline: 2px solid black;}`.

By default, browsers add an outline around buttons and other controls when they are clicked:

![](outline.gif)

Removing the outline by setting `*:focus {outline: none;}` will make the site [less accessible for keyboard users](http://outlinenone.com/).

`focus-outline-manager` enables you to remove the outline for mouse users, retaining it for keyboard users.

## Demo

- [View JSBin demo](https://jsbin.com/yonofu/edit?html,css,output)

## Install

    npm install --save focus-outline-manager

## Usage

Using CommonJS module loading:
```javascript
require('focus-outline-manager');
```

CSS:
```css
.focus-outline-hidden :focus {
    outline: none;
}
```

## Credits

- `focus-outline-manager` is based on a Chromium UI utility [focus-outline-manager.js](https://chromium.googlesource.com/chromium/src/+/master/ui/webui/resources/js/cr/ui/focus_outline_manager.js) (Copyright © 2012, The Chromium Authors).

## Other Implementations

- https://github.com/csmr/classy-focus.js
- https://github.com/kimmobrunfeldt/fix-outline
- https://github.com/ambassify/smart-outline
- https://github.com/ry5n/keyring
- https://github.com/lindsayevans/outline.js
