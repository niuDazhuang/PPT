<template>
  <h3 class="view2-title">This is View2</h3>
</template>
<script>
  export default {
    mounted () {
      this.$emit('view', this.meta())
    },

    preFetch () {
      return this.methods.meta()
    },

    methods: {
      meta () {
        return {
          title: 'view2 title',
          h1: 'view2 - view2',
          description: 'this is view2 description',
          keywords: 'view, view2'
        }
      }
    }
  }
</script>