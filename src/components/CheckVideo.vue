<template>
  <div class="checkbox_wrapper">
    <input
      type="checkbox"
      class="checkbox"
      v-for="(item, i) of videos"
      :key="i"
      @click="selectVideo(i)"
      :checked="index == i ? true : false"
    />
  </div>
</template>

<script>
export default {
  props: ["videos", "index", "pathName"],
  methods:{
    selectVideo(i){
      const list = document.querySelectorAll('.video_wrapper video');
      list.forEach(a => {
        a.currentTime = 0;
      })
      this.$emit('selectVideo', i)
    }
  }
};
</script>
