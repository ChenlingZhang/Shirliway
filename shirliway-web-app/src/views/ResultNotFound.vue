<template>
    <div class="resultNotFound">
        <div class="header">
            <NaviBar />
        </div>

        <div class="body_notFound">
            <div class="notFoundWord">
                <span>We are unable to find any product that matches "abc"</span>
            </div>

            <div>
                <input type="button" class="backBtn" value="CHECK UP OTHER PRODUCT" @click="move2Product" />
            </div>
        </div>

        <div class="footer">
            <FootBar />
        </div>
    </div>
</template>

<style>
.resultNotFound {
    position: relative;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    min-height: 100%;
    padding-bottom: 100px;
    font-family: HarmonySans_Regular;
}

.body_notFound {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    padding-bottom: 120px;
    flex-direction: column;
}

.footer {
    position: absolute;
    bottom: 0;
    left: 0;
    height: 120px;
    width: 100%;
}

.notFoundWord {
    font-family: HarmonySans_Regular;
    font-size: 20px;
    font-weight: 500;
    line-height: 23px;
    letter-spacing: 0.2em;
    text-align: justify;
    margin-bottom: 123px;
}

.backBtn {
    width: 284px;
    height: 38px;
    flex-shrink: 0;
    background-color: #000;
    font-family: HarmonySans_Regular;
    color: #FFF;
    text-align: center;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    letter-spacing: 1.6px;
    text-transform: uppercase;
}
</style>

<script>
import NaviBar from '@/components/NavigationHeader.vue'
import FootBar from '@/components/CommonFooterBar.vue'

export default {
    name: 'AboutView',
    components: {
        NaviBar,
        FootBar
    },
    methods: {
        move2Product() {
            this.$router.push("/wood")
        }
    }
}
</script>