<template>
  <div>
    <logo/>
    <br>
    Enter any title above to access a note. No account required.<br>
    <br>
    Every note is public.  You are free to modify any note you see.<br>
    <br>
    Every note is encrypted.  You must know the title to see the note.<br>
    <br>
    Publicnote is <a href="https://github.com/routman/publicnote" target="_blank">open source</a> for full transparency<br>
    <br>
    Do not use publicnote to store sensitive information.<br>
    <br>
    publicnote &copy; 2019 - daniel@ncrypt.org
  </div>
</template>

<script>
import logo from './logo.vue'
export default {
  name: 'home',
  components: {
    logo
  }
}
</script>

<style scoped lang="scss">
@import "../assets/settings.scss";

</style>
