<template>
  <div id="wrapper">
    <main>
      
    </main>
  </div>
</template>

<script>
  export default {
    name: 'dashboard',
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style>

</style>
