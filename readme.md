# Accessibility <!-- omit in toc -->

When you are developing in an accessible way you are not only coding for completely blind people. There are a lot of people out there with low-vision who can still see the screen and for instance use their mouse to hover over text which is then read to them by the screen reader.

And we haven't even mentioned people who just prefer using `Tab` to go through a site/form.

Accessibility in general is much more than proper semantics, focus handling, contrasts.
Site speeds etc.

However, this page (for now) will only deal with the above.

- [Who uses screen readers?](#who-uses-screen-readers)
- [Handling focus](#handling-focus)
  - [Interactive elements](#interactive-elements)
  - [What's in focus?](#whats-in-focus)
- [Screen readers](#screen-readers)
  - [NVDA](#nvda)
  - [Alternatives to NVDA](#alternatives-to-nvda)
    - [JAWS](#jaws)
    - [Voice Over](#voice-over)
    - [Narrator](#narrator)
    - [Screen reader - Chrome extension](#screen-reader---chrome-extension)
    - [ChromeVox](#chromevox)
    - [Ubuntu](#ubuntu)
- [Resources, tutorials, tools](#resources-tutorials-tools)
  - [Udacity + Google course](#udacity--google-course)
  - [W3's wai tutorials](#w3s-wai-tutorials)
  - [Van11y scripts](#van11y-scripts)
  - [Tools](#tools)

## Who uses screen readers?
76% of screen reader users are blind (from a [non-representative study](https://webaim.org/projects/screenreadersurvey8/#disability)). The rest have either low vision (18.5%) or other impairments (deafness/hard-of-hearing	6.0%, cognitive 3.3%, motor 2.0% and other). 15% have multiple disabilities.

## Handling focus
Any element that's in the tab order (can be reached when you `Tab` through the site) can receive focus.

### Interactive elements

`<div>`s are not focusable by default, you have to place them in the tab order if you want them to behave as interactive elements such as buttons.

```html
<div tabindex="0">Tabbable due to tabindex value of 0.</div>
```

[MDN article on tabindex](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex)

### What's in focus?

If you lose sight of the focus ring and are not sure what element is currently in focus you can find it through your dev tools the following way:

1. Open Dev Tools (`Ctrl` + `Shift` + `I`)
2. Select `Console`
3. Click on `Live expressions`
4. Type `document.activeElement`
5. Click outside of the Live Expression UI to save.

## Screen readers

Check out the [screen reader guide page](/nvda.md) for help on how to set up and use a screen reader on your own machine. It helps a lot in checking the accessibility of your code.

### NVDA
The recommended software to be used. It is free, works on Windows machines and widely used.

### Alternatives to NVDA
In order of popularity based on a [non-representative survey done by WebAim](https://webaim.org/projects/screenreadersurvey8/)

#### JAWS
If you have it, use it. It is widely used but not free.

#### Voice Over
If you are on a Mac machine you should have access to Voice Over which is a great piece of tech.

#### Narrator
Windows10's inbuilt screen reader - Narrator - is not very good and not really used by many. Avoid using it.

#### Screen reader - Chrome extension
A Google developed Chrome extension (previously called ChromeVox). OK for quick checks but not very comprehensive or widely used.

#### ChromeVox
ChromeOS's screen reader, not widely used (just like ChromeOS 🙄)

#### Ubuntu
In `Settings` under `Universal access` there's a toggle for a screen reader. It's OK but not very widely used.


## Resources, tutorials, tools

### Udacity + Google course
If you want a comprehensive overview of accessibility and implementation in the codebase this is a great course to go through. Touches on everything important from focus handling to the importance of proper semantics and aria attributes amongst others.\
https://www.udacity.com/course/web-accessibility--ud891

### W3's wai tutorials

Great, practical examples of accessible code patterns from tables and forms to images and carousels.\
https://www.w3.org/WAI/tutorials/

### Van11y scripts

A collection of accessible vanilla JS scripts for carousels, tab panels, accordions, hide/shows, modal windows, dialog tooltips (modal) and tooltips.\
https://van11y.net/

### Tools

It's improtant to note that automatic tools, whilst useful, are not at all a subsitute to manual evaluation. According to a [government accessibility tool audit](https://alphagov.github.io/accessibility-tool-audit/) the best evaluators catch at most 40% of issues.

#### HTML Validator <!-- omit in toc -->

npm package for in development validation.

https://www.npmjs.com/package/html-validator

#### W3 Html markup validator<!-- omit in toc -->

copy paste your code or URL for validation

https://validator.w3.org/

#### Web Accessibility Evaluation Tool (WAVE)<!-- omit in toc -->

Run an accessibility check on a page to see all issues.

https://wave.webaim.org/

#### Arc Toolkit, Axe DevTools<!-- omit in toc -->

Similar to WAVE, can be added as browser plugins as well.

#### Contrast checker<!-- omit in toc -->

For a quick check whether a design has proper contrast.

https://webaim.org/resources/contrastchecker/
