# Vuetify Icon Picker

This is an vuetify component used to pick [material design icons](https://materialdesignicons.com/).

## Preface

Are you once troubled by no icon-picker component when using framework [vuetify](https://vuetifyjs.com/)?

If yes here is one possible solution!

## Getting Started

### Installing

```shell
npm i vuetify-icon-picker
```

### Using

In an common 2.x vuetify project (and `mdi` has been imported by way html cdn-link or `npm i @mdi/font`), you can use this component as following:

```vue
<template>
  <icon-picker v-model="selected" />
</template>

<script>
import IconPicker from "./components/IconPicker.vue";

export default {
  components: {
    IconPicker
  },
  data: () => ({
    selected: ""
  })
};
</script>
```

You can find more detailed example in [this REPO](https://github.com/taoqingqiu/vuetify-icon-picker)

## Component API

### Props

| Name          | Type     | Default   | Description                                                  |
| ------------- | -------- | --------- | ------------------------------------------------------------ |
| contentHeight | `number` | 300       | used to specify one certain height of the container of icons |
| value         | `string` | undefined | the chosen icon, looks like `mdi-home-outline`               |

### Events

| Name  | Description                                                 |
| ----- | ----------------------------------------------------------- |
| input | together with prop `value`, to cater to `v-model` directive |
