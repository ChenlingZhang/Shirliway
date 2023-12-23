<template>
    <div class="product">
        <div>
            <span>This is {{ productType }} page</span>
        </div>
    </div>
</template>

<style></style>

<script>
export default {
    data() {
        return {
            productType: '',
            productBannerURL:{
                'wood': '',
                'marble': '',
                'pattren': '',
                'soildcolor'
            }
        }
    },

    methods: {
        getProductType() {
            console.log('oncall')
            var currentPattern = window.location.hash.split('?')[1];
            console.log(currentPattern)
            this.productType = decodeURIComponent(currentPattern.split('=')[1]);
            console.log(this.productType)
        },
        setBannerImgURL(){

        }
    },

    mounted: function () {
        this.getProductType();
    }
}
</script>