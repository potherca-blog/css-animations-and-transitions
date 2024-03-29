# CSS Animations and Transitions

For the [Muze Dev Day][1], I want to make a simple example for each CSS animation and transition.

## Animatable CSS properties

> Certain CSS properties can be animated using CSS Animations or CSS Transitions. Animation means that their values can be made to change gradually over a given amount of time.

_<sup>
Source: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties
</sup>_

Besides `all`, these properties are:

- `accent-color`
- `backdrop-filter`
- `background`
    - `background-color`
    - `background-position`
    - `background-size`
- `block-size`
    - `max-block-size`
    - `min-block-size`
- `border`
    - `border-bottom`
    - `border-left`
    - `border-right`
    - `border-top`
    - `border-color`
        - `border-bottom-color`
        - `border-left-color`
        - `border-right-color`
        - `border-top-color`
    - `border-width`
        - `border-bottom-width`
        - `border-left-width`
        - `border-right-width`
        - `border-top-width`
    - `border-radius`
        - `border-bottom-left-radius`
        - `border-bottom-right-radius`
        - `border-end-end-radius`
        - `border-end-start-radius`
        - `border-start-end-radius`
        - `border-start-start-radius`
        - `border-top-left-radius`
        - `border-top-right-radius`
    - Border Block
        - `border-block-end`
        - `border-block-end-color`
        - `border-block-end-width`
        - `border-block-start`
        - `border-block-start-color`
        - `border-block-start-width`
    - `border-image-outset`
    - `border-image-slice`
    - `border-image-width`
    - Border Inline
        - `border-inline-end`
        - `border-inline-end-color`
        - `border-inline-end-width`
        - `border-inline-start`
        - `border-inline-start-color`
        - `border-inline-start-width`
- `bottom`
- `box-shadow`
- `caret-color`
- `clip`
- `clip-path`
- `color`
- Column
    - `column-count`
    - `column-gap`
    - `column-rule`
    - `column-rule-color`
    - `column-rule-width`
    - `column-width`
    - `columns`
- `filter`
- Flex
    - `flex`
    - `flex-basis`
    - `flex-grow`
    - `flex-shrink`
- Font
    - `font`
    - `font-size`
    - `font-size-adjust`
    - `font-stretch`
    - `font-variation-settings`
    - `font-weight`
    - `letter-spacing`
    - `line-height`
    - `word-spacing`
- Grid
    - `gap`
    - `grid-column-gap`
    - `grid-gap`
    - `grid-row-gap`
    - `grid-template-columns`
    - `grid-template-rows`
- `height`
    - `max-height`
    - `min-height`
- `inline-size`
    - `max-inline-size`
    - `min-inline-size`
- Inset
    - `inset`
    - `inset-block`
    - `inset-block-end`
    - `inset-block-start`
    - `inset-inline`
    - `inset-inline-end`
    - `inset-inline-start`
- `left`
- Margin
    - `margin`
        - `margin-bottom`
        - `margin-left`
        - `margin-right`
        - `margin-top`
    - `margin-block-end`
    - `margin-block-start`
    - `margin-inline-end`
    - `margin-inline-start`
- `mask`
    - `mask-border`
    - `mask-position`
    - `mask-size`
- `object-position`
- `offset`
    - `offset-anchor`
    - `offset-distance`
    - `offset-path`
    - `offset-position`
    - `offset-rotate`
- `opacity`
- `order`
- `outline`
    - `outline-color`
    - `outline-offset`
    - `outline-width`
- Padding
    - `padding`
        - `padding-bottom`
        - `padding-left`
        - `padding-right`
        - `padding-top`
    - `padding-block-end`
    - `padding-block-start`
    - `padding-inline-end`
    - `padding-inline-start`
- `perspective`
- `perspective-origin`
- `right`
- `rotate`
- `row-gap`
- `scale`
- Scroll
    - Scroll Margin
        - `scroll-margin`
        - `scroll-margin-block`
        - `scroll-margin-block-end`
        - `scroll-margin-block-start`
        - `scroll-margin-bottom`
        - `scroll-margin-inline`
        - `scroll-margin-inline-end`
        - `scroll-margin-inline-start`
        - `scroll-margin-left`
        - `scroll-margin-right`
        - `scroll-margin-top`
    - Scroll Padding
        - `scroll-padding`
        - `scroll-padding-block`
        - `scroll-padding-block-end`
        - `scroll-padding-block-start`
        - `scroll-padding-bottom`
        - `scroll-padding-inline`
        - `scroll-padding-inline-end`
        - `scroll-padding-inline-start`
        - `scroll-padding-left`
        - `scroll-padding-right`
        - `scroll-padding-top`
    - `scroll-snap-coordinate`
    - `scroll-snap-destination`
    - `scrollbar-color`
- Shape
    - `shape-image-threshold`
    - `shape-margin`
    - `shape-outside`
- `tab-size`
- Text
    - `text-decoration`
    - `text-decoration-color`
    - `text-decoration-thickness`
    - `text-emphasis`
    - `text-emphasis-color`
    - `text-indent`
    - `text-shadow`
    - `text-underline-offset`
- `top`
- `transform`
- `transform-origin`
- `translate`
- `vertical-align`
- `visibility`
- `width`
    - `max-width`
    - `min-width`
- `z-index`
- `zoom`

## Transitions

Starting with transitions, I have two axis:

1. CSS properties that can be animated
2. CSS transition properties

The `transition` CSS property is shorthand for:

- `transition-delay` takes a `<time>`
- `transition-duration` takes a `<time>`
- `transition-property` any property listed in the "Animatable CSS properties"
  section
- `transition-timing-function` takes an `<easing-function>`

### Easing functions

- **`cubic-bezier(p1, p2, p3, p4)`**
  An author-defined cubic-Bezier curve, where the p1 and p3 values must be in
  the range of 0 to 1.
- **`ease`** _(the default)_
  Equal to cubic-bezier(0.25, 0.1, 0.25, 1.0), the default value, increases in
  velocity towards the middle of the transition, slowing back down at the end.
- **`ease-in`**
  Equal to cubic-bezier(0.42, 0, 1.0, 1.0), starts off slowly, with the
  transition speed increasing until complete.
- **`ease-out`**
  Equal to cubic-bezier(0, 0, 0.58, 1.0), starts transitioning quickly, slowing
  down the transition continues. •
- **`ease-in-out`**
  Equal to cubic-bezier(0.42, 0, 0.58, 1.0), starts transitioning slowly, speeds
  up, and then slows down again.
- **`linear`**
  Equal to cubic-bezier(0.0, 0.0, 1.0, 1.0), transitions at an even speed.
- **`steps( n, <jumpterm>)`**
    - **`jump-start`** or **`start`**
      Denotes a left-continuous function, so that the first jump happens when
      the transition begins;
    - **`jump-end`** or **`end`**
      Denotes a right-continuous function, so that the last jump happens when
      the animation ends;
    - **`jump-none`**
      There is no jump on either end. Instead, holding at both the 0% mark and
      the 100% mark, each for 1/n of the duration
    - **`jump-both`**
      Includes pauses at both the 0% and 100% marks, effectively adding a step
      during the transition time.
- **`step-start`**
  Equal to steps(1, jump-start)
- **`step-end`**
  Equal to steps(1, jump-end)

### `<time>`

- either a positive or a negative number
- either an integer or a float
- use a unit (`ms` for milliseconds, `s` for seconds)
- zero `0` MUST be `0ms` or `0s` to be valid

_<sup>
Source: https://developer.mozilla.org/en-US/docs/Web/CSS/time
</sup>_

[1]: https://muze-nl.github.io/dev-day/
