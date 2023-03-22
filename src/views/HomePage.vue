<template>
  <div class="kv">
    <div class="right">
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
    </div>
    <div class="top"></div>
    <div class="left">
      <div class="box-l">
        <img
          :src="require('../assets/images/zapladnaya_sibir.svg')"
          alt="rink"
          class="rink-l"
        />
        <router-link class="btn" to="/sibir">
          ЗАПАДНАЯ СИБИРЬ - МОСКВА <br />
          <span>(вторая половина XX века)</span>
        </router-link>
      </div>
    </div>
    <div class="bottom">
      <div class="b-box">
        <img
          :src="require('../assets/images/baku_santpeterburg.svg')"
          alt="rink"
          class="rink-b"
        />
        <router-link class="btn" to="/baku">
          БАКУ - САНКТ-ПЕТЕРБУРГ <br />
          <span> (конец XIX века - начало XX века)</span>
        </router-link>
      </div>
    </div>
    <span class="circle">
      <h3>КАК ПРОЛЕГАЛ ПУТЬ НЕФТИ В РАЗНЫЕ ЭПОХИ?</h3>
      <p>Чтобы узнать, выберите маршрут и коснитесь его названия</p>
    </span>
  </div>
</template>
