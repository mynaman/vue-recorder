<template>
    <div class="login" v-show="isHidden">
        <div class="login_container">
            <div class="container">
                <div class="close">
                    <button type="button" class="close_btn" >
                        <span @click.stop="closeContainer">&times;</span>
                    </button>
                </div>
                <form class="login_form">
                    <label for="exampleInputEmail1">Email address</label>
                    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Email">
                    <label for="exampleInputPassword1">Password</label>
                    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
                    <button type="submit" class="btn btn-dark">Login</button>
                </form>
                <div class="login_line">
                    <span>or</span>
                </div>
                <div class="auth-btn">
                    <h3>소셜 로그인</h3>
                    <button class="btn facebook"><font-awesome-icon :icon="{ prefix: 'fab', iconName: 'facebook-f' }"/></button>
                    <button class="btn google"><font-awesome-icon :icon="{ prefix: 'fab', iconName: 'google' }"/></button>
                    <button class="btn kakao">KAKAO</button>
                </div>
                <div class="company">
                  <div class="company_line">
                      <span></span>
                  </div>
                  <div class="company_security">
                    <ul class="list_links">
                        <li><a href="#">이용약관</a></li>
                        <li><a href="#">개인정보처리방침</a></li>
                    </ul>
                    <div class="corp">
                      <span>ⓒ A mocha Corp.</span>
                    </div>
                  </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ['isHidden'],
  methods: {
    closeContainer: function () {
      this.$emit('isContainer')
    }
  }
}
</script>

<style scoped lang="scss">
.login{
    display: block;
    position: fixed;
    top:0;
    right:0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.4);
    z-index: 999;
    cursor: default;

    .login_container{
        position: absolute;
        background-color: #fff;
        width: 100%;
        height: 100%;
        right: 0;
        overflow-y: auto;
        animation-name: move;
        animation-duration: 0.2s;

        @keyframes move {
            from {
                width: 0;
            }
            to {
                width: 100%;
            }
        }
        .container{
            display: flex;
            flex-direction: column;
            margin: 0 20px;

            .close {
                .close_btn {
                    width: 100%;
                    margin-bottom: 3.5rem;
                    font-size: 4.5rem;
                    outline-style: none;
                    border:0;
                    background-color: #fff;
                    text-align: right;
                    span{
                        color: #979797;
                        cursor: pointer;
                    }
                }
            }
            .login_form{
                padding: 0 6px;
                display: flex;
                justify-content: flex-start;
                flex-direction: column;
                label{
                    text-align: left;
                    color: #000;
                    margin-bottom: 6.4px;
                }
                input{
                    margin-bottom: 20px;
                    padding: .375rem .35rem;
                    font-size: 1rem;
                    line-height: 1.5;
                    color: #495057;
                    background-color: #fff;
                    border:0;
                    border-bottom: 1px solid #ced4da;
                    border-radius: .25rem;
                    outline-style: none;
                }
                button[type="submit"] {
                    margin-bottom: 20px;
                    padding: .375rem .75rem;
                    font-size: 1rem;
                    font-weight: bold;
                    line-height: 1.5;
                    color:#000;
                    background-color: #fff;
                    border: 1px solid #ced4da;
                    border-radius: .25rem;
                    cursor: pointer;
                    letter-spacing: 0.5px;
                    outline: none;
                }
                button[type="submit"]:hover {
                    background-color: powderblue;
                    color: #fff;
                }
            }

            .login_line{
                text-align: center;
                position: relative;
                overflow: hidden;
                span{
                  display: inline-block;
                  vertical-align: middle;
                  position: relative;
                  color: #665f5a;
                  padding: 0 .75rem;
                }
                span:before{
                  right: 100%;
                }
                span:after{
                  left: 100%;
                }
                span:before, span:after{
                  content: '';
                  display: block;
                  position: absolute;
                  width: 1000px;
                  top: 50%;
                  border-top :1px solid #a19b97;
                }
            }
            .auth-btn{
                h3{
                    color: #000;
                }
                .btn{
                    display: block;
                    width: 100%;
                    margin-bottom: 20px;
                    padding: .375rem .75rem;
                    font-size: 1rem;
                    font-weight: bold;
                    line-height: 1.5;
                    color:#fff;
                    background-color: #fff;
                    border: 0;
                    border-radius: .25rem;
                    cursor: pointer;
                    letter-spacing: 0.5px;
                    outline: none;
                }

                .facebook {
                    background-color: #39579a;
                }
                .facebook:hover {
                    background-color: #304a83;
                }
                .google {
                    background-color: #c9171e;
                }
                .google:hover {
                    background-color: #b4141b;
                }
                .kakao {
                    background-color: #fcea00;
                }
                .kakao:hover {
                    background-color: #e6d600;
                }
            }
            .company{
              display: block;
              .company_line{
                  text-align: center;
                  position: relative;
                  overflow: hidden;
                  span{
                    display: inline-block;
                    vertical-align: middle;
                    position: relative;
                    color: #665f5a;
                    padding: 0 .75rem;
                  }
                  span:before{
                    right: 0%;
                  }
                  span:before, span:after{
                    content: '';
                    display: block;
                    position: absolute;
                    width: 1000px;
                    top: 50%;
                    border-top :1px solid #a19b97;
                  }
              }
              .company_security{
                text-align: left;
                .list_links{
                  margin:0;
                  padding:0;
                  li{
                    margin: 20px 0;
                    a{
                      text-decoration: none;
                      color: #000;
                      font-size: 17px;
                    }
                  }
                }
              }
              .corp{
                // position: absolute;
                padding-bottom: 20px;
                bottom: 0;
                color: #828282;
                font-size: 15px;
              }
            }
            @media (min-width: 768px){
              .company{
                display: none;
              }
            }

        }
    }
    @media (min-width: 768px){
        .login_container{
            width: 22vw;
            animation-name: move;
            animation-duration: 0.2s;
        }

        @keyframes move {
            from {
                width: 0;
            }
            to {
                width: 22vw;
            }
        }
    }
}
</style>
