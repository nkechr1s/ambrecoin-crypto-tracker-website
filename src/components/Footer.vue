<template>
  <v-footer class="footer">
    <div class="footer-top">
      <div class="data-provider">
        <p>
          Data provided by
          <a
            target="_blank"
            rel="noreferrer nofollow"
            href="https://coingecko.com"
            >CoinGecko</a
          >
        </p>
        <div class="coin-gecko-logo"></div>
      </div>
      <v-spacer></v-spacer>
    </div>

    <div class="footer-bottom">
      {{ new Date().getFullYear() }} — <strong>ambrecoin.com</strong>
    </div>
  </v-footer>
</template>

<style>
.footer {
  display: flex;
  flex-direction: column;
  margin-top: 80px;
}

.footer-top {
  border-bottom: 1px solid #333;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;
  color: white;
}

.footer-icon {
  margin-right: 1rem;
}

.footer-bottom {
  text-align: center;
  padding: 1rem 0;
  color: white;
}

.coin-gecko-logo {
  position: relative;
  background-image: url("../assets/coingeckgo.png");
  display: inline-block;
  background-position: 100%;
  background-repeat: no-repeat;
  background-size: contain;
  width: 25px;
  height: 25px;
}

.data-provider {
  display: flex;
  align-items: center;
  gap: 10px;
  width: 100%;
  justify-content: flex-end;
}

.data-provider p {
  font-size: 12px;
}
.data-provider a {
  color: #9ce7bd;
}
</style>
