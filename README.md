[![Build Status](https://travis-ci.org/tecbeast42/autocomplete-vue.svg?branch=master)](https://travis-ci.org/tecbeast42/autocomplete-vue)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![npm](https://img.shields.io/npm/v/autocomplete-vue.svg)](https://www.npmjs.com/package/autcomplete-vue)
[![npm](https://img.shields.io/npm/dt/autocomplete-vue.svg)](https://www.npmjs.com/package/autcomplete-vue)


# Autocomplete-vue

autocomplete-vue is a vue component build with webpack
If you want to include the .vue file instead of a compiled webpack js file you can use the file at `src/js/autocomplete-vue.vue`.

## Usage

A demo is available in demo/demo.html.

### Initialize Autocomplete-vue

```
import AutocompleteVue from 'autocomplete-vue';

Vue.component('autocomplete-vue', AutocompleteVue);
```

### Use the Component

```
<autocomplete-vue
    :list="[{name: 'item1'}, {name: 'item2'}, {name: 'item3'}]"
    placeholder="Autocomplete"
></autocomplete-vue>

<autocomplete-vue
    classPrefix="my-custom-class"
    url="/my-list/all"
    requestType="get"
></autocomplete-vue>

<autocomplete-vue
    v-model="input"
    url="/countries/all"
    requestType="get"
    property="capital"
    :required="true"
    :threshold="1"
></autocomplete-vue>

<autocomplete-vue
    url="/important/all"
    requestType="post"
    :ignoreCase="false"
></autocomplete-vue>
```

## Properties

### classPrefix

   Sets prefix for the styling class (override)
  * type: String,
  * required: false
  * default: 'autocomplete

### url

   An url to load the list from
  * type: String,
  * required: false

### requestType

   The request type for the url
  * type: String,
  * required: false

### list

   A list of objects that the input should be compared to
  * type: Array,
  * required: false

### property

   The property in the list that the autocomplete will compare
  * type: String,
  * required: false,
  * default: 'name'

### placeholder

   A placeholder text for the input field
  * type: String,
  * required: false

### inputClass

   Specifies a class for the input field
  * type: String,
  * required: false

### required

   If the input field is required when submitting a form
  * type: Boolean,
  * required: false,
  * default: false

### ignoreCase

   If set to false, the autocomplete will be case sensitive ('a' doesn't match 'A')
  * type: Boolean,
  * required: false,
  * default: true

### threshold

   The number of characters required for the autocomplete-list to show
   Setting a negative number will make the list visible all the time (with focus)
  * type: Number,
  * required: false,
  * default: 0

### value

   The value that is set when using v-model on the component
  * required: false

## Installation

```
npm install --save autocomplete-vue
yarn add autocomplete-vue
```
