<template>
    <div class="footer">
        <div class="footer_container">
            <div class="container">
                <div class="inner_footer">
                    <a href="#">ⓒ A mocha Corp.</a>                
                    <ul class="list_links">
                        <li><a href="#">이용약관</a></li>
                        <li><a href="#">개인정보처리방침</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {        
    }
</script>

<style scoped lang="scss">

.footer{
    display: block;
    height: 110px;
    border-top: 1px solid #eee;
    bottom: 0;

    .footer_container{        
        .container{
            .inner_footer{                
                margin: 20px auto 0 auto;                
                padding: 0 40px;
                width: 1000px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                font-size: 14px;
                line-height: 14px;
                
                a{
                    display: inline-block;
                    font-size: 1.0rem;
                    color: #333;
                    text-decoration: none;
                }
                .list_links{
                    margin: 0;
                    padding: 0;                    
                    list-style: none;
                    
                    li{
                        margin: 0 20px;
                        float: left;
                        padding: 12px 0;
                        display: list-item;
                        list-style: none;
                        color: #888;
                        font-family: 'Nanum Gothic Coding', monospace, sans-serif;

                        a{
                            display: inline-block;
                            font-size: 0.843rem;
                            font-weight: 300;

                        }
                    }
                    
                    li:before{
                        content: '';
                        float: left;
                        width: 1px;
                        height: 13px;
                        margin: 0 20px 0 20px;
                        background-color: rgba(0, 0, 0, 0.2);                        
                    }
                }
            }
                
        }
    }
}

</style>