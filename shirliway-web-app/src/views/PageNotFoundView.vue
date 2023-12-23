<template>
    <div class="pageNotFound">
        <div class="head">
            <NaviBar />
        </div>

        <div class="body_pageNotFound">
            <div class="body_pageNotFound_word">
                <span>
                    The Information you want to know will be avaliable soon. and now you can browse other interesting
                    content.
                </span>
            </div>

            <div>
                <input type="button" class="backBtn" value="BACk TO HOMEPAGE" @click="move2Home" />
            </div>
        </div>

        <div class="footer">
            <FootBar />
        </div>
    </div>
</template>

<style>
.pageNotFound {
    position: relative;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    min-height: 100%;
    padding-bottom: 100px;
    font-family: HarmonySans_Regular;
}

.body_pageNotFound {
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

.body_pageNotFound_word {
    font-family: HarmonySans_Regular;
    color: #000;

    text-align: justify;
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: 40px;
    letter-spacing: 4px;
    margin-bottom: 123px;
    height: 80px;
    width: 755px;
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
        move2Home() {
            this.$router.push("/")
        }
    }
}
</script>