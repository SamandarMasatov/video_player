<template>
  <div class="video_page">
    <CheckVideo
      :videos="videos"
      :pathName="pathName"
      @selectVideo="changeVideo"
    />
    <PlayVideo :video="videos[index]" :pathName="pathName" />
  </div>
</template>

<script>
import PlayVideo from "@/components/PlayVideo";
import CheckVideo from "@/components/CheckVideo";
export default {
  components: {
    PlayVideo,
    CheckVideo,
  },
  data() {
    return {
      videos: [
        "7_0.mp4",
        "7.mp4",
        "8.mp4",
        "9.mp4",
        "10.mp4",
        "11_fixed.mp4",
        "11.mp4",
      ],
      index: 0,
      pathName: "sibir",
    };
  },
  methods: {
    changeVideo(index) {
      console.log(this.videos[index]);
      this.index = index;
    },
  },
};
</script>
