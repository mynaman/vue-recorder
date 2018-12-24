<template>
    <div class="menu">
        <div class="menu_container">
            <div class="container">
                <div class="company">
                    <a href="#">A mocha</a>
                </div>
                <div class="menu_list">
                    <ul>
                        <li>
                            <a href="#" @click.stop="openContainer">
                                Login
                                <login-bar :isHidden="isHidden" v-on:isContainer="closeContainer"></login-bar>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import LoginBar from './LoginBar'

export default {
  data: function () {
    return {
      isHidden: false
    }
  },
  methods: {
    openContainer: function () {
      this.isHidden = true
    },
    closeContainer: function () {
      this.isHidden = false
    }
  },
  components: {
    LoginBar
  }
}
</script>

<style scoped lang="scss">
.menu{
    position: absolute;
    top: 0;
    width: 100%;
    .menu_container{
        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 10px 20px;
            .company{
                a{
                    text-decoration: none;
                    color: #fff;
                    font-size: 30px;
                }
            }
            .menu_list{
                ul{
                    margin: 0;
                    padding: 0;
                    list-style: none;
                    li{
                        a{
                            text-decoration: none;
                            color: #fff;
                            font-size: 20px;
                        }

                        a:hover{
                            text-decoration: underline;
                        }
                    }
                }
            }
        }
    }
}
</style>
