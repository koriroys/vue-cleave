# Vue-Cleave
> forked from https://github.com/nosir/cleave.js

CleaveJS as a component of VueJS

## Run the example
```
git clone git@github.com:jrainlau/vue-cleave.git
cd vue-cleave && npm install
npm run dev
```

## VueJS component usage
Find the main file in `./src/App.vue` and `./src/components/cleave.vue`.
```
<!-- App.vue -->

<template>
  <Cleave :options='cleaveOptions' v-model='formatedValue'></Cleave>
</template>

<script>
import Cleave from './components/cleave.vue'

export default {
  data() {
    return {
      formatedValue: '',
      cleaveOptions: {
        numeral: true,
        numeralDecimalScale: 4
      }
    }
  },
  watch: {
    'formatedValue': (val) => {
      console.log(val)
    }
  },
  components: {
    Cleave
  }
}

</script>
```
By using `cleave.vue` as a component, there are three things for you to do:

1. Import `cleave.vue` and set as a component of the parent.
2. Pass in the custom `cleaveOptions` prop.
3. Simply use `<Cleave></Cleave>` as a normal `<input/>` field.

## Options
The options in `vue-cleave` are same as in the Doc below:
> [Cleave.js Documentation](https://github.com/nosir/cleave.js/blob/master/doc/options.md)

## License
Vue-Cleave is licensed under the [Apache License Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
- Cleave.js is included under its  [Apache License Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)

- Google libphonenumber is included under its  [Apache License Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
