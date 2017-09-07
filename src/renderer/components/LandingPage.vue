<template>
<div id="wrapper">
  <mu-appbar title="456Wings">
    <mu-text-field icon="search" class="appbar-search-field" slot="right" hintText="search for sth..." />
    <mu-flat-button color="white" icon='settings' label="Settings" slot="right" ref="button" @click="toggle" />
    <mu-popover :trigger="trigger" slot='right' :open="open" @close="handleClose">
      <mu-menu>
        <mu-menu-item title="Refresh" />
        <mu-menu-item title="Send feedback" />
        <mu-menu-item title="Settings" />
        <mu-menu-item title="Help" />
        <mu-menu-item title="Sign out" />
      </mu-menu>
    </mu-popover>
  </mu-appbar>
</div>
</template>

<script>
export default {
  data() {
    return {
      value: '3',
      open: false,
      trigger: null
    }
  },
  mounted() {
    this.trigger = this.$refs.button.$el
  },
  methods: {
    toggle() {
      this.open = !this.open
    },
    handleClose() {
      this.open = false
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

.appbar-search-field {
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

.menu-list {
  position: absolute;
  right: 0;
  top: 64px;
  width: 224px;
}

.demo-menu {
  width: 224px;
}
</style>
