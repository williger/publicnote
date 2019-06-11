<template>
  <div>
    <logo/>
    <br>
    Every note is encrypted with AES256, using the title as the encryption key.  An SHA256 hash of the title is used to index the encrypted note. The title is never exposed, thus neither the website owner nor the web host can view the plaintext contents of any note (unless the title is easily guessed).<br>
    <br>
    By design, there is no way to recover a note if you forget the title.<br>
    <br>
    Notes stored on publicnote can be public or private, depending on the complexity of the title. Simple titles lead to highly visible notes that can be edited by anyone who stumbles upon them, while complex titles lead to private, anonymous notes that are securely encrypted. The higher the complexity, the higher the privacy.<br>
    <br>
    Using common words like "hello" as the title is for entertainment purposes only.  You will find a variety of messages left by others.  If you find something you find offensive, delete it.<br>
    <br>
    <div class="link" @click="sot.title=''">home</div>
    <br><br>
  </div>
</template>

<script>
import logo from './logo.vue'
export default {
  name: 'howitworks',
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
