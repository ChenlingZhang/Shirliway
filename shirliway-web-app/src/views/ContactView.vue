<template>
    <div class="contact">
        <div class="header">
            <NaviBar />
        </div>

        <div class="body">
            <div class="contact_box">
                <div class="contact_image">
                    <el-image :src="require('@/static/img/contactpage/contactus.jpg')"
                        style="width: 500px; height: 500px;"></el-image>
                </div>
                <div class="contact_info" style="position: relative;">
                    <div class="first_row" style="width: 100%; margin-top: 77px; height: 55px; position: absolute;">

                        <el-row :gutter="37">
                            <el-col :span="12">
                                <span>First Name</span>
                                <el-input v-model="firstName"></el-input>
                            </el-col>

                            <el-col :span="12">
                                <span>Job Title</span>
                                <el-select v-model="value" placeholder="">
                                    <el-option v-for="item in options" :key="item.value" :label="item.label"
                                        :value="item.value">
                                    </el-option>
                                </el-select>
                            </el-col>
                        </el-row>
                    </div>

                    <div class="second_row" style="width: 100%; height: 55px; margin-top: 150px; position: absolute;">

                        <el-row :gutter="37">
                            <el-col :span="12">
                                <span>Email</span>
                                <el-input v-model="email"></el-input>
                            </el-col>

                            <el-col :span="12">
                                <span>Country</span>
                                <el-input v-model="country"></el-input>
                            </el-col>
                        </el-row>
                    </div>

                    <div class="thrid_row" style="width: 100%; height: 167px; margin-top: 243px; ">
                        <span class="third_row_word">What can we do for you ?</span>
                        <el-input type="textarea" :rows="7" v-model="requirement"></el-input>
                    </div>

                    <div class="final_row"
                        style="width: 100%; height: 37.8px; margin-top: 427px; position: absolute;">
                        <input type="button" value="submit" class="submit_btn" />
                    </div>
                </div>
            </div>

        </div>

        <div class="footer">
            <FootBar />
        </div>
    </div>
</template>

<style>
.contact {
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
    min-height: 100vh;
    padding-bottom: 120px;
    justify-content: center;
    align-items: center;
}

.footer {
    position: absolute;
    bottom: 0;
    left: 0;
    height: 120px;
    width: 100%;
}

.contact_box {
    width: 980px;
    height: 547px;
    border: black solid 1px;
    margin-top: 45px;
    display: flex;
    align-items: center;
}

.contact_image {
    width: 500px;
    height: 500px;
    margin: 23px auto 24px 18px;
}

.contact_info {
    width: 384px;
    height: 465px;
    margin-right: 25px;
    display: flex;
    justify-content: space-between;
}


.contact_info span {
    font-family: HarmonySans_Regular;
    color: #000;
    text-align: justify;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    letter-spacing: 1.6px;
    text-transform: capitalize;
}

.input_solot input {
    width: 159px;
    height: 35px;
}

.input_solot el-select {
    width: 159px;
    height: 35px;
}

.third_row_word {
    display: block;
    text-align: left !important;
    font-family: HarmonySans_Regular !important;
}

.submit_btn {
    width: 106.85px;
    height: 37.82px;
    top: 599px;
    left: 1042px;
    background: #000000;
    color: white;
    font-family: HarmonySans_Regular;
    font-size: 16px;
    font-weight: 400;
    line-height: 19px;
    letter-spacing: 0.1em;
    text-align: center;


}
</style>

<script>
import NaviBar from '@/components/NavigationHeader.vue'
import FootBar from '@/components/CommonFooterBar.vue'

export default {
    components: {
        NaviBar,
        FootBar
    },

    data() {
        return {
            options: [
                {
                    value: "Designer",
                    label: "Designer"
                },
                {
                    value: "Contacter",
                    label: "Contacter"
                },
                {
                    value: "User",
                    label: "User"
                },
                {
                    value: "Dealer",
                    label: "Dealer"
                }
            ],
            value: "",
            firstName: "",
            email: "",
            country: "",
            requirement: ""
        }
    }
}
</script>