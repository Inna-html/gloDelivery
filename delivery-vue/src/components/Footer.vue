<template>

  <footer class="footer">
        <div class="container">
          <div class="footer-box">
            <router-link to="/" class="footer-logo logo">
              <img src="../assets/img/logo.png" alt="logo" />
            </router-link>
            <div class="footer-nav">
              <ul>
                <li>Ресторанам</li>
                <li>Курьерам</li>
                <li>Пресс-центр</li>
                <li>Контакты</li>
              </ul>
            </div>
            <div class="footer-social">
              <img src="../assets/img/icon/inst.png" alt="instagram" />
              <img src="../assets/img/icon/fb.png" alt="facebook" />
              <img src="../assets/img/icon/vk.png" alt="vk" />
            </div>
          </div>
        </div>
</footer>

</template>

<script>
export default {

}
</script>

<style scoped>

.footer {
  min-height: 156px;
  display: flex;
  align-items: center;
  padding: 60px 0px;
}

.footer-box {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 36px;
}

.footer-logo {}

.footer-nav {
  flex-grow: 1;
}

.footer-nav ul {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: 15px;
}

.footer-nav ul li {
  color: #595959;
  font-size: 18px;
  font-weight: 400;
}

.footer-social {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 20px;
}

</style> 
