<template>
    <div class="m-home f-pr">
        <div class="u-logo f-pa">
            <img src="../assets/images/logo.png" alt="">
            <p class="version">cubeex - v1.0</p>
        </div>
        <div class="m-homeBtn f-pa">
            <div class="u-button u-demo f-pr" @click="goMenu">
                <div class="f-pa">
                    <span class="menu_icon f-fl"></span><span class="f-fl">Demo</span>
                </div>
            </div>
            <div class="u-button u-github f-pr">
                <div class="f-pa" @click="goGithub">
                    <span class="git_icon f-fl"></span><span class="f-fl">Github</span>
                </div>
            </div>
        </div>
        
    </div>
</template>
<script>
export default {
    name: 'home',
    data() {
        return {

        }
    },
    components: {
    },
    methods: {
        goMenu() {
            this.$router.push({ path : '/menu' });
        },
        goGithub() {
            location.href = "https://github.com/fangyongbao/cubeex";
        }
    },
    mounted: function() {

    }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
    .m-home {
        width: 100%;
        height: 100%;
        background: url(../assets/images/home_bg.jpg) top center no-repeat;
        background-size: cover;
        // padding-top: 45%;
        .u-logo {
            width: 100%;
            top: 25%;
            img {
                width: 1.7rem;
                display: block;
                margin: 0 auto;
            }
            .version {
                color: white;
                text-align: center;
                font-size: 18px;
                margin-top: 0.2rem;
            }
        }
        .m-homeBtn {
            width: 100%;
            bottom: 17%;
            .u-demo {
                background: #FFEA00;
                border: 1px solid #BDC1D2;
                color: #2D3859;
                .menu_icon {
                    width: 0.4rem;
                    height: 0.4rem;
                    background: url(../assets/images/icon/icon-demo.png) center no-repeat;
                    background-size: 0.4rem 0.4rem;
                    margin-right: 0.3rem;
                }
                div {
                    left: 2.47rem;
                }
            }
            .u-demo:active {
                background: darken(#FFEA00, 10%);
            }
            .u-github {
                background: #FFFFFF;
                border: 1px solid #BDC1D2;
                color: #2D3859;
                .git_icon {
                    width: 0.4rem;
                    height: 0.4rem;
                    background: url(../assets/images/icon/icon-github.png) center no-repeat;
                    background-size: 0.4rem 0.4rem;
                    margin-right: 0.24rem;
                }
                span {
                    line-height: 0.5rem;
                }
                div {
                    left: 2.47rem;
                }
            }
            .u-github:active {
                background: darken(#FFFFFF, 10%);
            }
        }
        .u-button {
            margin: 0 0.4rem 0.4rem;
            padding: 0.25rem 0;
            span {
                line-height: 0.4rem;
            }
        }
        .u-demo {

        }
    }
</style>
