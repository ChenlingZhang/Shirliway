<template>
    <div class="vision_case">
        <div class="head">
            <NavigationHeader />
        </div>

        <div class="vison_case_body">
            <div class="vision_case_banner">
                <el-image :src="require('@/static/img/visioncasepage/banner.jpg')"></el-image>
            </div>

            <div class="vision_case_common">
                <span>
                    We hope to bring the beauty of nature into the realm and space of people's lives, providing users with
                    sensory emotional resonance such as visual and tactile senses.
                </span>
            </div>

            <div class="vision_case_article">
                <div class="article">
                    <el-image class="article_img" :src="require('@/static/img/visioncasepage/commonspace.jpg')"></el-image>
                    <span class="article_title">COMMERICAL SPACE</span>
                </div>

                <div class="article">
                    <el-image class="article_img"
                        :src="require('@/static/img/visioncasepage/housecustomized.jpg')"></el-image>
                    <span class="article_title">HOUSE CUSTOMIZED</span>
                </div>

                <div class="article">
                    <el-image class="article_img" :src="require('@/static/img/visioncasepage/highend.jpg')"></el-image>
                    <span class="article_title">HIGH-END CUSTOM
                        FURNITURE</span>
                </div>
            </div>
        </div>



        <div class="footer">
            <CommonFooter />
        </div>
    </div>
</template>

<style>
.vision_case {
    position: relative;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    min-height: 100%;
    padding-bottom: 5%;
    font-family: HarmonySans_Regular;
}

.vison_case_body {
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
    padding-bottom: 120px;
}

.vision_case_banner {
    width: 100%;
    margin-bottom: 40px;
}

.vision_case_common {
    width: 1043px;
    height: 120px;
    font-family: HarmonySans_Regular;
    font-size: 20px;
    font-weight: 500;
    line-height: 40px;
    letter-spacing: 0.2em;
    text-align: justify;
    margin-bottom: 40px;
}

.vision_case_article {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.article {
    width: 337px;
    height: 546px;
    margin-right: 112px;
}

.article_img {
    width: 337px;
    height: 469px;
    margin-bottom: 54px;
}

.article_title {
    color: #000;
    text-align: justify;
    font-family: HarmonySans_Regular;
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    letter-spacing: 4px;
}

.footer {
    position: absolute;
    bottom: 0;
    left: 0;
    height: 120px;
    width: 100%;
}
</style>

<script>
import NavigationHeader from '@/components/NavigationHeader.vue'
import CommonFooter from '@/components/CommonFooterBar.vue'

export default {
    components: {
        NavigationHeader,
        CommonFooter
    }
}
</script>