# Vue Joyride

![NPM License](https://img.shields.io/npm/l/vue-joyride)

**Lightweight** tooltip component to explain new features of your [Vue](https://vuejs.org/) app **< 10k** 😎 <br>

![joyride](https://private-user-images.githubusercontent.com/91323932/270128117-cf45f263-9710-40fb-b18f-5fbf26069c8c.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTEiLCJleHAiOjE2OTU0OTU4NDgsIm5iZiI6MTY5NTQ5NTU0OCwicGF0aCI6Ii85MTMyMzkzMi8yNzAxMjgxMTctY2Y0NWYyNjMtOTcxMC00MGZiLWIxOGYtNWZiZjI2MDY5YzhjLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFJV05KWUFYNENTVkVINTNBJTJGMjAyMzA5MjMlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjMwOTIzVDE4NTkwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTQ1NGI2NWFhYWM4ZmRiM2Q2M2Y2MjRlMjZiMDZkMGRlZjc5NDkyNDVlM2YwODkwNjgyMjFiNDAxYjgwNTE3MDAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.BiHESLa7L1s6COkOESMZ9g2pV2RdonltnuceQxvoohg)

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

