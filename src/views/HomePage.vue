<template>
  <div class="kv">
    <div class="right_wrapper"></div>
    <!-- Timano -->
    <router-link
      to="/timano"
      class="right"
      :class="interval == 3 ? 'home_animation' : ''"
    >
      <router-link to="/timano">
        <div class="box-r">
          <img
            :src="require('../assets/images/timano_pechara.svg')"
            alt="rink"
            class="rink"
          />

          <router-link class="btn" to="/timano">
            ТИМАНО-ПЕЧОРА <br />
            МИРОВЫЕ РЫНКИ <span>(XXI век)</span>
          </router-link>
        </div>
      </router-link>
    </router-link>
    <div class="top"></div>
    <!-- Sibir -->
    <router-link
      to="/sibir"
      class="left"
      :class="interval == 1 ? 'home_animation' : ''"
    >
      <router-link to="/sibir" class="box-l">
        <img
          :src="require('../assets/images/zapladnaya_sibir.svg')"
          alt="rink"
          class="rink-l"
        />
        <router-link class="btn" to="/sibir">
          ЗАПАДНАЯ СИБИРЬ - МОСКВА <br />
          <span>(вторая половина XX века)</span>
        </router-link>
      </router-link>
    </router-link>
    <!-- baku -->
    <router-link
      to="/baku"
      class="bottom"
      :class="interval == 2 ? 'home_animation' : ''"
    >
      <router-link to="/baku" class="b-box">
        <img
          :src="require('../assets/images/baku_santpeterburg.svg')"
          alt="rink"
          class="rink-b"
        />
        <router-link class="btn" to="/baku">
          БАКУ - САНКТ-ПЕТЕРБУРГ <br />
          <span> (конец XIX века - начало XX века)</span>
        </router-link>
      </router-link>
    </router-link>
    <span class="circle">
      <h3>
        КАК ПРОЛЕГАЛ ПУТЬ <br />
        НЕФТИ В РАЗНЫЕ ЭПОХИ?
      </h3>
      <p>Чтобы узнать, выберите маршрут и коснитесь его названия</p>
    </span>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  data() {
    return {
      interval: 1,
    };
  },
  mounted() {
    setInterval(() => {
      if (this.interval == 3) {
        this.interval = 0;
      }
      this.interval++;
    }, 3600);
  },
};
</script>
