<template>
  <div class="checkbox_wrapper">
    <input
      type="checkbox"
      class="checkbox"
      v-for="(item, i) of videos"
      :key="i"
      @click="$emit('selectVideo', i)"
      :checked="index == i ? true : false"
    />
  </div>
</template>

<script>
export default {
  props: ["videos", "index", "pathName"],
};
</script>
