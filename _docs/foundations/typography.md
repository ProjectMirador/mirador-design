---
title: Typography
info: Roboto is intended as the primary font for Mirador 3.
---

## Sizes and styling
Below are the font sizes, weights, and letter-spacing for the classes defined here:
[https://material.io/develop/web/components/typography/](https://material.io/develop/web/components/typography/)

(Specify rems; px are for reference.)

class | rem | px | weight | line-height | letter-spacing | other
:--- | :--- | :--- | :--- | :--- | :--- | :---
Headline 1 | 2.822rem | 45.159 | 300 | 1.2em | -.015em
Headline 2 | 1.575rem | 25.192 | 300 | 1.33em | 0
Headline 3 | 1.383rem | 22.127 | 300 | 1.33em | 0
Headline 4 | 1.215rem | 19.436 | 400 | 1.45em | 0.007em
Headline 5 | 1.138rem | 18.215 | 400 | 1.55em | 0.005em
Headline 6 | 1.067rem | 17.072 | 400 | 1.6em | 0.01em
Subtitle 1 | 0.937rem | 14.995 | 300 | 1.6em | .015em
Subtitle 2 | 0.878rem | 14.053 | 500 | 1.75em | .02em
Body 1 | 1rem | 16px | 400 | 1.6em | 0
Body 2 | 0.878rem | 14.053 | 400 | 1.6em | .015em
BUTTON | 0.878rem | 14.053 | 500 | 2.25**rem** | 0.09em | uppercase
Caption | 0.772rem | 12.344 | 400 | 1.6**rem** | 0.033em
OVERLINE | 0.678rem | 10.842 | 500 | 2em | .166em | uppercase

## Classes

Some specific class assignments are needed to override default sizes.

element | assign class
:--- | :---
window title `<h2>` | Heading 6
companion window `<h3>` | Subtitle 1
`<dt>` |  Subtitle 2
`<dd>` | Body 1
"Current item" etc. labels in About panel | OVERLINE
window dialog `<h3>` | Heading 2 (we don't have any of these yet)

## Samples

<img width="367" alt="typography" src="https://user-images.githubusercontent.com/6945691/53993257-ba5e3200-40e3-11e9-953f-838a575ea21b.png">



## Fallback

A `sans-serif` fallback font is used in case [@font-face](https://www.w3schools.com/cssref/css3_pr_font-face_rule.asp) is not supported in the target browser.

---

## Copyright

Roboto is free software. For more details, visit Google Fonts official website at [https://fonts.google.com/](https://fonts.google.com/)
