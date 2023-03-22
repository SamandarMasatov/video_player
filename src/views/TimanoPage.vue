<template>
  <div class="video_page">
    <CheckVideo
      :videos="videos"
      :pathName="pathName"
      @selectVideo="changeVideo"
    />
    <PlayVideo :video="videos[index]" :pathName="pathName" @nextVideo="nextVideo" />
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
      console.log(this.videos[index]);
      this.index = index;
    },
    nextVideo(){
      this.index++;
    }
  },
};
</script>
