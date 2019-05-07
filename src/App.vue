<template>
  <div id="app">
    <input type="text" v-model="sot.title" placeholder="title" v-on:keyup="get()" autocapitalize="none"/>
    <status id="status"/>
    <home id="home" v-if="sot.title == ''"/>
    <terms id="terms" v-else-if="sot.title == 'terms'"/>
    <textarea placeholder="type note here" v-else v-model="sot.note" v-on:keyup="save()" v-bind:class="{blur: sot.loading}" :disabled="sot.loading == true"/>
  </div>
</template>

<script>

import home   from './components/home.vue'
import terms  from './components/terms.vue'
import status from './components/status.vue'

export default {
  name: 'app',
  components: {
    home, terms, status,
  },
  data: function() {
    return {
      sot: this.$root.$data,
    }
  },
  methods: {
    get: function() {
      clearTimeout(this.sot.autoload);
      clearTimeout(this.sot.autosave);
      if (this.sot.title != '' && this.sot.title != 'terms') {
        this.sot.get(this.sot.title);
      }
      else {
        this.sot.note = '';
        this.sot.status = '';
      }
    },
    save: function() {
      this.sot.save(this.sot.title, this.sot.note);
    }
  }
}
</script>

<style lang="scss">
@import "assets/settings.scss";

html, body {
  font-family: $font;
  color: $color-text;
  margin: 0;
  width: 100%;
  height: 100%;
}

#app {
  width: 100%;
  height: 100%;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

#home, #terms {
  flex-grow: 1;
  margin: $app-margin;
  overflow-y: scroll;
  -webkit-overflow-scrolling: touch;
}

#status {
  position: absolute;
  top: $app-margin;
  right: $app-margin;
}

.blur {
  filter:blur(2px);
  background: #FFFFFF;
}

input, textarea {
  display: block;
  font-family: $font;
  caret-color: $color-primary;
  font-size: 16px;
  border: none;
  border-radius: 0;
  box-sizing: border-box;
}
input:focus, textarea:focus {
  outline: none;
  border: none;
}
input {
  flex-grow: 0;
  min-height: 40px;
  width: calc(100% - 24px);
  border-bottom: 1px solid $color-primary;
  border-width: 0 0 1px 0 ;
  border-image: linear-gradient(to right, $color-primary 0%, $color-inactive 100%);
  border-image-slice: 1;

  margin: $app-margin;
  padding: 0;
}
input:focus {
  border-bottom: 1px solid $color-accent;
  border-width: 0 0 1px 0 ;
  border-image: linear-gradient(to right, $color-accent 0%, $color-primary 100%);
  border-image-slice: 1;
}
textarea {
  flex-grow: 1;
  width: 100%;
  padding-top: 16px;
  padding: $app-margin;
  line-height: 20px;
  overflow-y: scroll;
  -webkit-overflow-scrolling: touch;
}

.link {
  text-decoration: underline;
  display: inline-block;
  cursor: pointer;
  color: $color-primary;
}

</style>
