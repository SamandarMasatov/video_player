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
      videos: ["1_0.mp4", "1.mp4", "2.mp4", "3.mp4", "4.mp4", "5.mp4", "6.mp4"],
      index: 0,
      pathName: "baku",
    };
  },
  methods: {
    changeVideo(index) {
      console.log(this.videos[index]);
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
