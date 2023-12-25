<template>
  <div class="about">
    <div class="header">
      <NaviBar />
    </div>

    <div class="about_body">
      <div class="banner">
        <el-image :src="require('@/static/img/aboutuspage/shirliway.jpg')"></el-image>
      </div>

      <div class="article_p1">
        <span class="article_p1_title">
          Chapter of Origin
        </span>
        <div class="article_p1_body">
          Born from the ancient English meaning "from the dazzling Ranch", the meaning of SHIRLIWAY is "A smooth avenue
          under the sunshine". It is expected to carry the beautiful life of people, bring the natural aesthetics and
          experience to you, and become the link between things.
        </div>
      </div>

      <div class="vedio">
        <div class="vedio_container">
          <el-image :src="require('@/static/img/aboutuspage/vedio.jpg')" class="vedio_img" id="vedio_img"></el-image>
          <input type="button" class="vedio_button" value="VIEW OUR VEDIO" id="vedioButton" @click="
          route2socialmedia(
            'https://www.youtube.com/channel/UC2Rh0YK-HhucDx8ITmaQgxA'
          )
        "/>
        </div>
      </div>

      <div class="gallary">
        <div class="gallary_title">
          <span>Gallary</span>
        </div>

        <div>
          <el-carousel style="width: 1000px; height: 500px;">
            <el-carousel-item>
              <el-image :src="require('@/static/img/aboutuspage/gallery.jpg')"
                style="width: 100%; height: 100%; object-fit: cover;"></el-image>
            </el-carousel-item>
          </el-carousel>
        </div>
      </div>

      <div class="find">
        <div class="find_article">
          <span>
            From the deep yearning for nature, we are committed to creating excellent products, so that it can realize the
            harmonious integration of nature and human beings in the living space, environmental protection and
            sustainable development is not only the continuation of our yearning for nature, but also our commitment to
            nature; At the same time, we uphold the spirit of innovation, continue to explore and optimize the production
            process, just like the four seasons of nature, and continue to breed new possibilities. It is this
            innovation-driven culture that enables us to continuously provide more valuable products and work tirelessly
            to create a better world.
          </span>
        </div>

        <div class="find_img">
          <el-image :src="require('@/static/img/aboutuspage/find.jpg')"></el-image>
        </div>

      </div>

      <div class="locate">
        <div class="locate_title">
          <span>Browse to find a SHIRLIWAY office near you.</span>
        </div>
      </div>
    </div>



    <div class="footer">
      <FootBar />
    </div>
  </div>
</template>

<style>
.about {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  min-height: 100%;
  padding-bottom: 100px;
  font-family: HarmonySans_Regular;
}

.about_body {
  display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
    padding-bottom: 120px;
}

.footer {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 120px;
  width: 100%;
}

.banner {
  width: 100%;
}

.banner .el-image {
  width: auto;
  height: auto;
}

.article_p1 {
  margin-top: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  align-content: center;
}

.article_p1_title {
  font-family: HarmonySans_Bold;
  font-size: 36px;
  font-weight: 700;
  line-height: 42px;
  letter-spacing: 0.1em;
  text-align: justify;

}

.article_p1_body {
  margin-top: 40px;
  width: 842px;
  height: 96px;
  text-align: justify;
  font-family: HarmonySans_Regular;
  font-size: 16px;
  font-weight: 400;
  line-height: 32px;
  letter-spacing: 0.1em;

}

.vedio_container {
  position: relative;
  margin-bottom: 40px;
  margin-top: 40px;
}

.vedio_img {
  width: 1000px;
  height: 500px;
}

.vedio_button {
  visibility: hidden;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: opacity 0.5s, visibility 0.5s;
}

.vedio_button {
  width: 352px;
  height: 51px;
  flex-shrink: 0;
  border-radius: 15px;
  border: 3px solid #FFF;
  background: rgba(255, 255, 255, 0.00);
  font-family: HarmonySans_Regular;
  color: #FFF;
  text-align: center;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  letter-spacing: 4px;
  text-transform: uppercase;

}

.vedio_img:hover+.vedio_button,
.vedio_button:hover {
  visibility: visible;
  opacity: 1;
  /* 鼠标悬停时显示按钮 */
}

.gallary {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  align-content: center;
  margin-bottom: 40px;
}

.gallary_title {
  font-family: HarmonySans_Bold;
  font-size: 36px;
  font-weight: 700;
  line-height: 42px;
  letter-spacing: 0.1em;
  text-align: justify;
  margin-bottom: 40px;

}

.el-carousel__container {
  height: 500px !important;
}

.find {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  align-content: center;
  margin-bottom: 40px;
}

.find_article {
  width: 842px;
  height: 256px;
  font-family: HarmonySans_Regular;
  font-size: 16px;
  font-weight: 400;
  line-height: 32px;
  letter-spacing: 0.1em;
  text-align: justify;
  margin-bottom: 40px;

}

.find_img {
  width: 1000px;
  height: 250px;
}

.locate {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  align-content: center;
  margin-top: 40px;
  margin-bottom: 40px;
}

.locate_title {
  font-family: HarmonySans_Regular;
  font-size: 20px;
  font-weight: 500;
  line-height: 23px;
  letter-spacing: 0.2em;
  text-align: justify;

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

  mounted() {
    var exploreImage = document.getElementById('vedioImage');
    var exploreButton = document.getElementById('vedioButton');

    if (exploreImage && exploreButton) {
      exploreImage.addEventListener('mouseenter', function () {
        exploreButton.style.visibility = 'visible'; // 显示按钮
      });

      exploreImage.addEventListener('mouseleave', function () {
        exploreButton.style.visibility = 'hidden'; // 隐藏按钮
      });
    }
  },

  methods: {
    route2socialmedia(url) {
      window.location.href = url;
    },
  },
}
</script>