<template>
  <div class="home">
    <menu-bar></menu-bar>
    <div class="home_container">
      <div class="container">
        <div class="cont1">
          <div class="context">
            <h1>녹음한 내용을 글로 보고 편집 하세요</h1>
            <a href="#" class="link_store">Google Play</a>
          </div>
        </div>
        <div class="cont2">
          <div class="context">
            <strong class="txt_info">일상속에 녹음 기능을 스마트하게 쓰기 위한 <em>스마트 녹음기</em></strong>
            <p class="desc_info">현재의 녹음 기능은 조금 더 편리해져야 되고, 그 방법도 더 다양해져야 한다고 생각합니다.</p>
            <p class="desc_info">수 많은 녹음 음성 파일을 쉽고 빨리 찾을수 있도록 한다면 소중한 시간은 짧게 단축 시킬수 있고 생산성을 극대화 시킬수 있습니다.</p>
            <p class="desc_info">소중한 시간은 길어지고 할 수 있는 일은 더 많아진다고 믿습니다</p>
            <p class="desc_info">모카한잔이 만들어 가는 ‘스마트녹음기’는 더 가치 있는 일상을 만드는 일입니다.</p>            
          </div>
        </div>
      </div>
    </div>
    <footer-bar></footer-bar>
  </div>
</template>

<script>
import MenuBar from '@/components/MenuBar'
import FooterBar from '../components/FooterBar'

export default {
  components: {
    MenuBar,
    FooterBar
  }
}
</script>

<style scoped lang="scss">
.home{
  .home_container{
    .container{
      width: 100%;
      height: 100%;
      .cont1{
        height: 680px;
        background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.2)), url('../img/analogue-antique-audio-290657.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        .context{
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
      .cont2{
        margin:0 30px;
        padding: 95px 40px 0;
        height: 240px;
        .context{
          .txt_info{
            margin: 0 auto 21px;
            height: 40px;
            display: block;
            text-align: center;
            font-size: 1.7rem;
            font-weight: normal;
            font-family: 'Nanum Gothic Coding', monospace, sans-serif;
            color: #333;
            em{
              font-weight: bold;
              font-style: normal;
            }
          }
          .desc_info{
            margin: 0;
            font-weight: 200;
            font-size: 16px;
            line-height: 27px;
            color: #666;
            text-align: center;
            font-family: 'Nanum Gothic Coding', monospace, sans-serif;
          }
        }
      }
    }
  }
}
</style>
