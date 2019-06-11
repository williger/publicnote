<template>
  <div>
    <logo/>
    <br>
    Enter any title above to access a note. No account required.<br>
    <br>
    Every note is public.  You are free to modify any note you find.<br>
    <br>
    Every note is encrypted.  You must know the title to see the note.<br>
    <br>
    There are a variety of uses for publicnote:
    <ul>
      <li>personal note-taking</li>
      <li>copy-pasting text from one device to another</li>
      <li>accessing notes from a public computer</li>
      <li>sending messages privately and anonymously</li>
      <li>chatting with strangers</li>
      <li>posting jokes and ASCII art</li>
      <li>puzzles and scavenger hunts</li>
      <li>announcements and advertisements</li>
      <li>wasting time</li>
    </ul>
    Publicnote is <a class="link" href="https://github.com/routman/publicnote" target="_blank">open source</a> for full transparency. Learn more about <div class="link" @click="sot.title = 'how it works'">how it works</div>.<br>
    <br>
    By using publicnote, you are agreeing to our <div class="link" @click="sot.title = 'terms'">terms of service</div>.<br>
    <br>
    Do not use publicnote to store sensitive information.<br>
    <br>
    daniel@ncrypt.org<br>
    publicnote &copy; 2019<br>
    <br>
  </div>
</template>

<script>
import logo from './logo.vue'
export default {
  name: 'home',
  components: {
    logo
  },
  data: function() {
    return {
      sot: this.$root.$data
    }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/settings.scss";

</style>
