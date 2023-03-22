<template>
  <div class="checkbox_wrapper">
    <div
      class="checkbox"
      v-for="(item, i) of videos"
      :key="i"
      @click="$emit('selectVideo', i)"
      :class="index == i ? 'checkbox_active':''"
    >
      <video class="video_checkbox" muted preload="metadata">
        <source
          :src="require(`../assets/video/${pathName}/${item}`)"
          type="video/mp4"
        />
      </video>
    </div>
  </div>
</template>

<script>
export default {
  props: ["videos", 'index', "pathName"],
};
</script>
