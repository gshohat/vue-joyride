# Vue Joyride

![NPM License](https://img.shields.io/npm/l/vue-joyride)

**Lightweight** [Vue](https://vuejs.org/) component to explain new features of your app **< 5k** 😎 <br>



## Usage

`npm i vue-joyride`

```
<script setup>
import Joyride from 'vue-joyride';
import 'vue-joyride/dist/style.css';

const steps = [
  { content: '1st Vue logo modal', target: '#logo'},
  { content: '2nd Vue logo modal', target: '#logo-2'},
];

const isAppMounted = ref(false);

onMounted(() => {
  isAppMounted.value = true;
});
</script>


<template>
<Joyride :steps="steps" v-if="isAppMounted"/>
</template
```


## Contact
Feel free to ping me 💫
<br>
connect@giladshohat.com

[giladshohat.com](https://giladshohat.com)

