<template>
  <div class="rating">
    <ul class="list">
     <li :key="star" v-for="star in maxStars" :class="{ 'active': star <= stars }" @click="rate(star)" class="star">
        <icon v-test="{ id: 'icon' }" scale="2" :name="star <= stars ? 'star' : 'regular/star'"/>
      </li>
    </ul>
    <span>{{ stars }} of {{ maxStars }}</span>
  </div>
</template>

<script>
  import 'vue-awesome/icons/star'
  import 'vue-awesome/icons/regular/star'

  import Icon from 'vue-awesome/components/Icon'

  export default {
    components: { Icon },
    data() {
      return {
        stars: 3,
        maxStars: 5
      }  
    },
    methods: {
      rate(star) {
        this.stars = star
      }
    }
  }
</script>

<style scoped>
  .rating {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    font-size: 14px;
    color: #a7a8a8;
  }
  .list {
    margin: 0 0 5px 0;
    padding: 0;
    list-style-type: none;
  }
  .list:hover .star {
    color: #f3d23e;
  }
  .star {
    display: inline-block;
    cursor: pointer;
  }
  .star:hover ~ .star:not(.active) {
    color: inherit;
  }
  .active {
    color: #f3d23e;
  }
</style>