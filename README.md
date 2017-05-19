# Simple Vue Form

A Vue.js component for make ajax form ease.

## Install

``` bash
$ npm install simple-vue-form
```
## Usage
```html
<template>
    <simple-vue-form :action="'/api/post'" @ajaxSuccess="formSuccess" @ajaxError="formError">
    //You must specify post url in :action="" with single quotes like conventional html5 form.
      <input name="title"/>
      <textarea name="body"></textarea>
      <input type="submit"/>
    </simple-vue-form>
</template>

<script>
import simpleVueForm from 'simple-vue-form'

export default {
  components: {
    'simple-vue-form': simpleVueForm
  },
  methods: {
    formSuccess (response) {
      // response of the success ajax post
    },
    formError (response) {
      // response of the fail ajax post
    }
  }
}
</script>
```
#### The json request post looks like

```
{
    'title': 'Awesome Post',
    'body': 'Lorem ipsum dolor sit amet.'
}