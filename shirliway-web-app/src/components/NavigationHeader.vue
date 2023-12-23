<template class="common_header">
  <div>
    <el-menu class="navi_bar" mode="horizontal" ref="main_navi" @select="handleSelection">
      <el-menu-item>
        <el-image :src="require('../static/img/logo.png')" fit="fit" alt="#" class="company-logo" @click="back2Home" />
      </el-menu-item>

      <el-submenu index="1">
        <template slot="title" @click="move2Product('product')">PRODUCTS</template>
        <el-menu-item index="1-1">WOOD</el-menu-item>
        <el-menu-item index="1-2">MARBLE</el-menu-item>
        <el-menu-item index="1-3">PATTERN</el-menu-item>
        <el-menu-item index="1-4">SOILD COLOR</el-menu-item>
        <el-menu-item index="1-5">ELEMENT</el-menu-item>
      </el-submenu>

      <el-submenu index="2">
        <template slot="title" >TECHNOLOGY</template>
        <el-menu-item index="2-1">PAGENNI-TECH</el-menu-item>
        <el-menu-item index="2-2">PASSYA TOUCH</el-menu-item>
        <el-menu-item index="2-3">DEMENSION</el-menu-item>
        <el-menu-item index="2-4">DU EDGE BAND</el-menu-item>
        <el-menu-item index="2-5">PERFORMANCE</el-menu-item>
        <el-menu-item index="2-6">FINISHED</el-menu-item>
      </el-submenu>

      <el-submenu index="3">
        <template slot="title">INSPIRATION</template>
        <el-menu-item index="3-1">VISION CASE</el-menu-item>
        <el-menu-item index="3-2">LIFESTYLE</el-menu-item>
        <el-menu-item index="3-3">CATALOG</el-menu-item>
        <el-menu-item index="3-4">LOOKBOOK</el-menu-item>
      </el-submenu>

      <el-menu-item index="4">CONTACT US</el-menu-item>

      <el-menu-item index="5">SHIRLIWAY</el-menu-item>

      <div class="search">
        <el-menu-item>
          <el-input placeholder="search......" class="nav-search-bar" v-model="search_input">
            <i slot="suffix" class="el-icon-search" @click="search_handle()"></i>
          </el-input>
        </el-menu-item>
      </div>
    </el-menu>
  </div>
</template>

<style>
.common_header {
  font-family: HarmonySans_Regular;
}

.navi_bar {
  width: 100%;
  height: 80px;
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
  font-size: 50px;
}

.company-logo {
  position: absolute;
  width: 83px;
  height: 72px;
  left: 0px;
  top: 0px;
  padding-left: 0%;
  padding-top: 0px;
  margin-top: 0px;
}

.el-submenu,
.el-menu-item {
  display: flex;
  outline: 1px;
  outline-color: #929292;
  outline-width: 1px;
  justify-content: center;
  align-content: center;
  align-items: center;
  font-size: 20px;
}

.el-dialog {
  width: 60%;
  height: 60%;
}

.el-dialog__body {
  width: 100%;
  height: 100%;
}

.el-submenu__icon-arrow {
  display: flex;
  color: #929292;
  justify-content: center;
  padding-left: 10px;
}

.appFrame {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
</style>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      search_input: "",
      visible: false,
      app_path: "https://calendly.com/hplshirliway/make-an-appointment-to-shirliway",
      router_dic: {
        'wood': '/wood',
        'marble': '/marble',
        'pattren': '/pattren',
        'soild color': '/soild_color',
        'finished': '/finished',
        'performance': '/performance',
        'pagenni-tech': '/pagenni-tech',
        'vision-case': '/vision_case',
        'lookbook': '/lookbook',
        'lifestyle': '/lifestyle',
        'contact': '/contact',
        'about': '/about',
        'notFound': '/resultNotFound',
        'pageNF': '/pageNotFound',
        'catalog': '/catalog'
      }
    };
  },

  methods: {
    back2Home() {
      this.$router.push("/");
      console.log("back 2 home");
    },

    move2Product(productType) {
      var push_requ = '/product?productType=' + productType;
      this.$router.push(push_requ)
    },

    move2Contact() {
      this.routerMove("/contact")
    },

    search_handle() {
      console.log(this.search_input);
    },

    handleSelection(index) {
      var tempname = ''
      if (index === '1-1') {
        this.move2Product('wood')
      }
      else if (index === '1-2') {
        this.move2Product('marble')
      }
      else if (index === '1-3') {
        this.move2Product('pattren')
      }
      else if (index === '1-4') {
        this.move2Product('soild color')
      }
      else if (index === '1-5') {
        this.routerMove('pageNF')
      }
      else if (index === '2-1') {
        this.routerMove('pagenni-tech')
      }

      else if (index === '2-2' || index === '2-3' || index === '2-4') {
        this.routerMove('pageNF')
      }

      else if (index == '2-5') {
        this.routerMove('performance')
      }

      else if (index == '2-6') {
        this.routerMove('finished')
      }

      else if (index === '3-1') {
        this.routerMove('vision-case')
      }
      else if (index === '3-2') {
        this.routerMove('lifestyle')
      }
      else if (index === '3-3') {
        this.routerMove('catalog')
      }
      else if(index==='3-4') {
        this.routerMove('lookbook')
      }
      else if (index === '4') {
        this.routerMove('contact')
      }
      else if (index === '5') {
        this.routerMove("about")
      }
    },

    routerMove(name) {
      var path = this.router_dic[name]
      console.log(path)
      this.$router.push(path)
    },
  },
};
</script>
