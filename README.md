# Vue Joyride

![NPM License](https://img.shields.io/npm/l/vue-joyride)

**Lightweight** tooltip component to explain new features of your [Vue](https://vuejs.org/) app **< 10k** 😎 <br>

![joyride](https://private-user-images.githubusercontent.com/91323932/270127779-31216a57-a0d0-477f-936d-a5d3a7e03737.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTEiLCJleHAiOjE2OTU0OTU0MTEsIm5iZiI6MTY5NTQ5NTExMSwicGF0aCI6Ii85MTMyMzkzMi8yNzAxMjc3NzktMzEyMTZhNTctYTBkMC00NzdmLTkzNmQtYTVkM2E3ZTAzNzM3LmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFJV05KWUFYNENTVkVINTNBJTJGMjAyMzA5MjMlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjMwOTIzVDE4NTE1MVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTQ0NTY1N2Q5NGE3OTI5NTE5ZTFiMTY1MWI0ZDJlYWEzMGFhNDdmYmZmNzU2MTdmYmZkZmRkMWM5MWJiMjhlMTYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.TpOd8FFMtWzT7PF_KgnjCH1qPFfneU0M5Lfrvm_RaVY)

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

