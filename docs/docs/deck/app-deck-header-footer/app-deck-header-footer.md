# Header &amp; Footer

Header and footer can be added to a [DeckDeckGo] deck or to any slides using their dedicated slots `header` and `footer`.

## Table of contents

- [Introduction](#app-deck-header-footer-introduction)
- [Slides](#app-deck-header-footer-slides)
- [Theming](#app-deck-header-footer-theming)

## Introduction

These elements are useful if you wish to display your brand or company logo on each slides.

To achieve this behavior, you can provide a slot `header` or `footer` to the deck, these are going to be cloned into each slides of your presentation at runtime.

```
<deckgo-deck>
  <deckgo-slide-title>
    <h1 slot="title">My presentation title</h1>
    <p slot="content">
      Hello World 🚀
    </p>
  </deckgo-slide-title>

  <div slot="header"><img data-src="./assets/mylogo.png"/></div>
  <div slot="footer"><a href="https://deckdeckgo.com">DeckDeckGo</a></div>
</deckgo-deck>
```

## Slides

If you want to display a specific `header` and `footer` on a particular slide, you proceed as displayed above but on the slide level.

```
<deckgo-deck>
  <deckgo-slide-title>
    <h1 slot="title">My presentation title</h1>
    <p slot="content">
      Hello World 🚀
    </p>

    <div slot="header"><img data-src="./assets/mylogo.png"/></div>
    <div slot="footer"><a href="https://deckdeckgo.com">DeckDeckGo</a></div>
  </deckgo-slide-title>
</deckgo-deck>
```

In case you would like to have `header` and `footer` defined for your deck but also assign specific ones on a particular slide, use the following attributes:

| Attribute     | Type    | Default | Description                                            |
| ------------- | ------- | ------- | ------------------------------------------------------ |
| custom-header | boolean | false   | Set to `true` to defined a specific header for a slide |
| custom-footer | boolean | false   | Set to `true` to defined a specific footer for a slide |

For example:

```
<deckgo-deck>
  <deckgo-slide-title custom-header custom-footer>
    <h1 slot="title">My presentation title</h1>
    <p slot="content">
      Hello World 🚀
    </p>

    <div slot="header"><img data-src="./assets/my-special-logo.png"/></div>
    <div slot="footer"><img data-src="./assets/my-special-footer.png"/></div>
  </deckgo-slide-title>

  <div slot="header"><img data-src="./assets/mylogo.png"/></div>
  <div slot="footer"><a href="https://deckdeckgo.com">DeckDeckGo</a></div>
</deckgo-deck>
```

## Theming

The following theming options will affect the slot `header` and `footer`.

| CSS4 variable                  | Default    | Note                                                       |
| ------------------------------ | ---------- | ---------------------------------------------------------- |
| --slide-header-footer-z-index  | -1         |                                                            |
| --slide-header-max-height      | 48px       | On devices smaller as `1024px` the default value is `16px` |
| --slide-header-justify-content | flex-start |                                                            |
| --slide-header-margin-top      | 16px       |                                                            |
| --slide-header-margin-end      | 32px       |                                                            |
| --slide-header-margin-bottom   | 16px       |                                                            |
| --slide-header-margin-start    | 32px       |                                                            |
| --slide-footer-max-height      | 32px       |                                                            |
| --slide-footer-justify-content | center     |                                                            |
| --slide-footer-margin-top      | 16px       |                                                            |
| --slide-footer-margin-end      | 16px       |                                                            |
| --slide-footer-margin-bottom   | 16px       |                                                            |
| --slide-footer-margin-start    | 16px       |                                                            |

[deckdeckgo]: https://deckdeckgo.com
