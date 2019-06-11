<template>
  <div>
    <div class="logo accent">public</div>
    <div class="logo">note</div>
    <div class="subtitle">&nbsp;&#124; public encrypted notepad</div>
  </div>
</template>

<script>
export default {
  name: 'logo'
}
</script>

<style scoped lang="scss">
@import "../assets/settings.scss";

.logo {
  display: inline-block;
  font-size: 16px;
  letter-spacing: 2px;
}

.accent {
  color: $color-primary;
  margin-right: 3px;
}

.subtitle {
  display: inline-block;
}

</style>
