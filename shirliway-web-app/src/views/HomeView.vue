<template>
  <div class="home">
    <div class="header">
      <NaviBar />
    </div>

    <div class="body">
      <!--Homepage Banner-->
      <div class="banner" style="width: 100%;">
        <el-carousel height="500px" width="100%">
          <el-carousel-item>
            <transition name="fade" appear>
              <el-image :src="require('@/static/img/homepage/banner/shirliway_banner1.jpg')"
                style="height: auto;"></el-image>
            </transition>
          </el-carousel-item>
        </el-carousel>

      </div>

      <!--shirliway 字样-->
      <div class="main">
        <div class="title">
          <span>SHIRLIWAY</span>
        </div>

        <div class="level2">
          <span>The Aesthetic Connection between Nature and Life. </span>
        </div>

        <div class="explore">
          <div class="explore_container">
            <el-image :src="require('@/static/img/homepage/explore.jpg')" class="explore_img"
              id="exploreImage"></el-image>
            <input type="button" class="explore_button" value="explore our story" id="exploreButton"
              @click="move2About()" />
          </div>
        </div>
        <div class="level3">
          <p>
            We are ultimately a part of nature, so our creations are also. We draw from nature and
            should also give feedback. We don't want the world to be filled with empty hustle and bustle, and the lush
            forests can't make its voice. We want to speak for it, and we don't want Shakespeare to say, 'The world is
            full of sound and enthusiasm, but there is nothing inside'
          </p>
        </div>
      </div>

      <!--Product Infomation-->
      <div class="product_info" style="margin-top: 40px;">
        <div class="product_info_title">
          <span>PRODUCT COLLECTION</span>
        </div>

        <div class="product_info_detail">
          <span>Check out our woods, marble & stones, patterns, solid colors, and combine them with our imagination to
            bring them into the real room, satisfying our wishes while also experiencing the natural and aesthetic
            connection of SHIRLIWAY.</span>
        </div>

        <div class="products_cat" style="display: flex;
  justify-content: center; /* 将子元素水平居中 */
  flex-wrap: wrap;">
          <div class="wood_product"
            style="display: flex; flex-direction: column; align-items: center; margin-right: 20px;">
            <el-image :src="require('@/static/img/homepage/products/WOODS.png')" class="product_image"></el-image>
            <span class="product_font">WOOD</span>
            <input type="button" value="MORE +" class="product_button" />
          </div>

          <div class="wood_product2"
            style="display: flex; flex-direction: column; align-items: center; margin-right: 20px;">
            <el-image :src="require('@/static/img/homepage/products/MARBLES.png')" class="product_image"></el-image>
            <span class="product_font">MARBLES</span>
            <input type="button" value="MORE +" class="product_button" />
          </div>

          <div class="wood_product3"
            style="display: flex; flex-direction: column; align-items: center; margin-right: 20px;">
            <el-image :src="require('@/static/img/homepage/products/PATTERNS.jpg')" class="product_image"></el-image>
            <span class="product_font">PATTERNS</span>
            <input type="button" value="MORE +" class="product_button" />
          </div>

          <div class="wood_product4" style="display: flex; flex-direction: column; align-items: center;">
            <el-image :src="require('@/static/img/homepage/products/SOILDCOLORS.jpg')" class="product_image"></el-image>
            <span class="product_font">SOILD COLORS</span>
            <input type="button" value="MORE +" class="product_button" />
          </div>
        </div>

        <div class="inspiration" style="margin-top: 40px">
          <el-image :src="require('@/static/img/homepage/INSPIRATION.jpg')"
            style="height: 500px; width: 1000px;"></el-image>
        </div>
      </div>
    </div>

    <div class="footer">
      <FootBar />
    </div>
  </div>
</template>


<style>
.home {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  min-height: 100%;
  padding-bottom: 100px;
  font-family: HarmonySans_Regular;
}

.body {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
  padding-bottom: 120px;
}

.el-carousel {
  width: 100%;
  /* 设置宽度为100% */
  height: 500px;
  /* 设置高度为500px，根据您的需求进行调整 */
}

.main {
  margin-top: 40px;
}

.title {
  font-family: HarmonySans_Bold;
  font-size: 36px;
  font-weight: 700;
  line-height: 42px;
  letter-spacing: 0.1em;
  text-align: justified;
  margin-bottom: 40px;

}

.level2 {
  margin-bottom: 40px;
  font-family: HarmonySans_Regular;
  font-size: 20px;
  font-weight: 500;
  line-height: 36px;
  letter-spacing: 0.2em;
  text-align: justified;

}

.explore_container {
  position: relative;
  margin-bottom: 40px;
}

.explore_button {
  visibility: hidden;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: opacity 0.5s, visibility 0.5s;
}

.explore_button {
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

.explore_img:hover+.explore_button,
.explore_button:hover {
  visibility: visible;
  opacity: 1;
  /* 鼠标悬停时显示按钮 */
}

.level3 {
  width: 842px;
  height: 149px;
  margin: 0 auto;
  /* 实现水平居中 */
  box-sizing: border-box;
  /* 包含内边距和边框在内的元素大小，避免超出框 */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: justify;

}

.level3 p {
  font-family: HarmonySans_Regular;
  color: #000;
  text-align: justify;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 32px;
  /* 200% */
  letter-spacing: 1.6px;
  margin-bottom: 40px;
}

.product_info {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}

.product_info_title {

  font-family: HarmonySans_Bold;
  font-size: 36px;
  font-weight: 700;
  line-height: 42px;
  letter-spacing: 0.1em;
  text-align: justify;
  margin-bottom: 40px;
}

.product_info_detail {
  width: 842px;
  height: 96px;
  margin: 0 auto;
  /* 实现水平居中 */
  box-sizing: border-box;
  /* 包含内边距和边框在内的元素大小，避免超出框 */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: justify;

  font-family: HarmonySans_Regular;
  font-size: 16px;
  font-weight: 400;
  line-height: 32px;
  letter-spacing: 0.1em;
  text-align: justify;

  margin-bottom: 40px;

}

.product_image {
  height: 331px;
  width: 235px;
  ;
}

.product_button {
  margin-top: 10px;
  width: 130px;
  height: 33px;
  border: 1px;
  border: 1px solid #000000;
  background-color: black;
  color: #FFF;
  text-align: center;
  font-family: HarmonySans_Regular;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  letter-spacing: 1.6px;
}

.product_font {
  font-family: HarmonySans_Regular;
  font-size: 20px;
  font-weight: 500;
  line-height: 23px;
  letter-spacing: 0.2em;
  margin-top: 10px;

}

.footer {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 120px;
  width: 100%;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
<script>
// @ is an alias to /src
import NaviBar from '@/components/NavigationHeader.vue'
import FootBar from '@/components/CommonFooterBar.vue'



export default {
  name: 'HomeView',
  components: {
    NaviBar,
    FootBar
  },

  methods: {
    move2About() {
      this.$router.push('/about');
    }
  },

  mounted() {
    var exploreImage = document.getElementById('exploreImage');
    var exploreButton = document.getElementById('exploreButton');

    if (exploreImage && exploreButton) {
      exploreImage.addEventListener('mouseenter', function () {
        exploreButton.style.visibility = 'visible'; // 显示按钮
      });

      exploreImage.addEventListener('mouseleave', function () {
        exploreButton.style.visibility = 'hidden'; // 隐藏按钮
      });
    }
  },
}
</script>