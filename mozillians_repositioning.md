# Mozillians repositioning front-end thoughts

Some personal thoughts on repositioning front-end. Where below there is a statement, please chime in and agree/disagree! :-) 

Goal: merge into one thing with Florian's document / other people's documents.

## General front-end practices

* We ensure our code complies to the Web Content Accessibility Guidelines (WCAG), so that Mozillians is usable by all and we comply with relevant legislation.
	* Example: our autocomplete works well with keyboard, screenreaders and dictation (with or without (some) WAI-ARIA)
* We prefer web platform features to library-specific workarounds
	* Example: we make sure form elements are in a `form` tag and submitting works (by pressing ENTER in an element, by firing `form.submit()`, by pressing GO on iOS, etc)
* We embrace progressive enhancement to make our code more resilient with things like feature detection
	* Examples: if we require geolocation to display something, we build the no-geo view first, make sure that is GOOD then add geo as an enhancement so that it is GREAT. An escalator is still stairs when the power is off.


## CSS

* We embrace the cascade where it makes sense.
* We write as little CSS as possible.
* No preprocessor, but we'll postprocess so that we can autoprefix.
* We use CSS Variables for colors.
* CSS lives outside the JS, we use ‘naming for scoping’, i.e. by sticking to unique names, we have workable enough ‘scopes’. 
* As a naming convention we follow BEM (block, element, modifier). Quick summary:
	* .block is a component
	* .block--modifier is a variation on the block component
	* .block__element is something inside the block component
* We make sure components look good (not the same) everywhere (in the devices, browsers, platforms our users use).

## Vue 

* _TBD_: templates with Vue templates or JSX? Native web components?
* _TBD_: state management with Vuex?
* _TBD_: routing: do we need it? If so, vue-router?
* _TBD_: front-end tests: Jest?
* _TBD_: node packages: npm or yarn?
* JS style guide: AirBnB


# Links 

Docs https://vuejs.org/v2/guide/ 
