# Svelte Material UI - Icon Button

Icon buttons are symbolic buttons or toggles.

See [MDC Icon Button](https://material.io/develop/web/components/buttons/icon-buttons/) for more information on API and Sass mixins.

See [the Sass variable file](https://github.com/material-components/material-components-web/blob/v3.1.1/packages/mdc-icon-button/_variables.scss) for styling variables.

# Installation

```sh
npm install --save-dev @svelte-material-ui/icon-button
```

# Basic Usage

```html
<script>
  import IconButton, {Icon} from '@svelte-material-ui/icon-button';

  let starred = false;

  function doSomething() {
    alert('something');
  }
</script>

<IconButton class="material-icons" on:click={doSomething}>build</IconButton>

<IconButton toggle bind:pressed={starred}>
  <Icon class="material-icons" on>star</Icon>
  <Icon class="material-icons">star_border</Icon>
</IconButton>
```

# Demo

*in action:* https://hperrin.github.io/svelte-material-ui-demo/#/icon-button

*demo code:* https://github.com/hperrin/svelte-material-ui-demo/blob/master/component-demos/IconButton.svelte

# Exports

## (default)

An icon button.

### Options / Defaults

* `use`: `[]` - An array of actions and/or action/property arrays.
* `class`: `''` - A CSS class string.
* `ripple`: `true` - Whether to implement a ripple for when the component is interacted with.
* `color`: `null` - A color passed to the ripple action.
* `toggle`: `false` - Whether the button is a toggle. A toggle button should have two `Icon` children, one with the `on` prop.
* `pressed`: `false` - Whether the toggle button is pressed.
* `href`: `null` - A hyperlink ref attribute. If this is present, the icon button will use an `a` element instead of a `button` element.

### Events

All standard UI events are forwarded.

* `MDCIconButtonToggle:change`

## Icon

A graphic icon.

See the [common icon readme](https://github.com/hperrin/svelte-material-ui/blob/master/common/README.md#icon).