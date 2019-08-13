<template>
  <div>
    <ul>
      <li><icon name="star" /></li>
      <li><icon name="star" /></li>
      <li><icon name="star" /></li>
      <li><icon name="regular/star" /></li>
      <li><icon name="regular/star" /></li>
    </ul>
    <span>3 of 5</span>
  </div>

</template>

<script>
  import 'vue-awesome/icons/star'
  import 'vue-awesome/icons/regular/star'

  import Icon from 'vue-awesome/components/Icon'

  export default {
    components: { Icon }
  }
</script>

<style>
  /* Your CSS goes here */
</style>