# Vue Joyride

![NPM License](https://img.shields.io/npm/l/vue-joyride)

**Lightweight** tooltip component to explain new features of your [Vue](https://vuejs.org/) app **< 10k** 😎 <br>

![joyride](https://github.com/gshohat/vue-joyride/assets/91323932/39e265b8-0efe-4ee3-95a7-dd72dc4c1bd3)

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

