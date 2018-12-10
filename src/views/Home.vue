<template>
  <div class="home">
    <menu-bar></menu-bar>
    <div class="home_container">
      <div class="container">
        <h1>녹음한 내용을 글로 보고 편집 하세요</h1>
        <a href="#" class="link_store">Google Play</a>
      </div>
    </div>
  </div>
</template>

<script>
import MenuBar from '../components/MenuBar'

export default {
  components: {
    MenuBar
  }
}
</script>

<style scoped lang="scss">
.home{
  .home_container{
    width: 100%;
    height: 680px;
    background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.2)), url('../img/analogue-antique-audio-290657.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    .container{
      position: relative;
      top: 50%;
      transform: translateY(-50%);

      h1{
        margin: 0;
        margin-bottom: 1.43rem;
        font-size: 4.5vw;
        color: #fff;
        font-family: 'Nanum Gothic Coding', monospace, sans-serif;
      }
      .link_store{
        display: inline-block;
        padding-left: 30px;
        width: 220px;
        height: 62px;
        text-decoration: none;
        color: #fff;
        border: 1px solid rgba(255,255,255,.3);
        border-radius: 5px;
        line-height: 62px;
        font-size: 1.2rem;
        text-align: center;
        background-image: url('../img/google_play.png');
        background-size: 1.9843rem;
        background-repeat: no-repeat;
        background-position: 50px 17px;
      }

      .link_store:hover {
        text-decoration: underline;

      }

      @media (min-width: 768px){
        h1{
        margin: 0;
        margin-bottom: 1.43rem;
        font-size: 2.5rem;
        color: #fff;
        font-family: 'Nanum Gothic Coding', monospace, sans-serif;
      }
      }
    }
  }
}
</style>
