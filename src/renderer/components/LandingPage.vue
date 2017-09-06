<template>
<div id="wrapper">
  <mu-appbar title="456Wings">
    <mu-text-field icon="search" class="appbar-search-field" slot="right" hintText="search for sth..." />
    <mu-flat-button color="white" label="Setting" slot="right" />
  </mu-appbar>
</div>
</template>

<script>
import SystemInformation from './LandingPage/SystemInformation'

export default {
  name: 'landing-page',
  components: {
    SystemInformation
  },
  methods: {
    open(link) {
      this.$electron.shell.openExternal(link)
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Source Sans Pro', sans-serif;
}
.appbar-search-field{
  margin-top: 12px;
}
.mu-text-field-hint {
  color: fade(#FFF, 54%);
}
.mu-text-field-input {
  color: #FFF;
}
.mu-text-field-focus-line {
  background-color: #FFF;
}
</style>
