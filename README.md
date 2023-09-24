# Vue Joyride

![NPM License](https://img.shields.io/npm/l/vue-joyride)

**Lightweight** tooltip component to explain new features of your [Vue](https://vuejs.org/) app **< 10k** 😎 <br>

![joyride](https://private-user-images.githubusercontent.com/91323932/270182320-9bfc2373-7a56-41e7-9b41-82a15c64f9b7.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTEiLCJleHAiOjE2OTU1NzgyMTAsIm5iZiI6MTY5NTU3NzkxMCwicGF0aCI6Ii85MTMyMzkzMi8yNzAxODIzMjAtOWJmYzIzNzMtN2E1Ni00MWU3LTliNDEtODJhMTVjNjRmOWI3LmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFJV05KWUFYNENTVkVINTNBJTJGMjAyMzA5MjQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjMwOTI0VDE3NTE1MFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTI4ZDY0MmNkYjk2ZjA5MjA5MzA2NmZjZjE0ZDI1ZjhiMWEyNjkxMDlkOWIzOWEyMmY3OTM1YjNhODUyNzQzMTcmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.jDCJpsQnSIRd4HNEoY9ESQNScGQR7ZFSU_ch-GgJu6k)

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

