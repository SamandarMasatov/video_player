<template>
  <div class="video_page">
    <CheckVideo
      :videos="videos"
      :index="index"
      :pathName="pathName"
      @selectVideo="changeVideo"
    />
    <PlayVideo
      :videos="videos"
      :index="index"
      :pathName="pathName"
      @nextVideo="nextVideo"
    />
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
      videos: ["12_0.mp4", "12.mp4", "13.mp4", "14.mp4", "15.mp4", "16.mp4"],
      index: 0,
      pathName: "timano",
    };
  },
  methods: {
    changeVideo(index) {
      this.index = index;
    },
    nextVideo() {
      if (this.index != this.videos.length - 1) {
        this.index++;
      } else {
        this.index = 0;
      }
    },
  },
};
</script>
