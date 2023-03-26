<template>
  <div
    class="video_wrapper"
    v-for="(item, i) of videos"
    :key="i"
    :class="index == i ? 'd-block video_active' : ' '"
  >
    <video
      class="video"
      id="checkVideo"
      :src="require(`../assets/video/${pathName}/${item}`)"
      autoplay
      muted
      type="video/mp4"
    ></video>
    <router-link to="/">
      <div class="home_icon_wrapper">
        <svg
          width="80"
          height="80"
          viewBox="0 0 307 296"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <rect
            x="21.524"
            y="119"
            width="96.2915"
            height="177"
            fill="#8E8E8E"
          />
          <rect
            x="189.185"
            y="119"
            width="96.2915"
            height="177"
            fill="#8E8E8E"
          />
          <rect
            x="21.5723"
            y="198.491"
            width="80"
            height="261.869"
            transform="rotate(-90 21.5723 198.491)"
            fill="#8E8E8E"
          />
          <path d="M153.5 0L286.435 120H20.5651L153.5 0Z" fill="#8E8E8E" />
        </svg>
      </div>
    </router-link>
    <button
      class="hide_button"
      @click="changeVidoe()"
      style="display: none"
    ></button>
  </div>
</template>

<script>
export default {
  props: ["videos", "index", "pathName"],
  emits: ["nextVideo"],
  methods: {
    changeVidoe() {
      const list = document.querySelectorAll('.video_wrapper video');
      list.forEach(a => {
        a.currentTime = 0;
      })
      this.$emit("nextVideo");
    },
  },
  mounted() {
    let videos = document.querySelectorAll(".video_wrapper video");
    let btn = document.querySelector('.hide_button');
    videos.forEach(a => {
      a.addEventListener('ended', function (){
        btn.click();
      })
    })
  },
};
</script>
