<template>
  <i class="iconfont icon-container" :class="fontClass"></i>
</template>
    
<script>
const classMap = {
    home: "icon-zhuye",
    success: "icon-zhengque",
    error: "icon-cuowu",
    close: "icon-guanbi",
    warn: "icon-jinggao",
    info: "icon-xinxi",
    blog: "icon-blog",
    code: "icon-code",
    about: "icon-set_about_hov",
    weixin: "icon-weixin",
    mail: "icon-email",
    github: "icon-GitHub",
    qq: "icon-qq",
    arrowUp: "icon-iconfonticonfonti2copy",
    arrowDown: "icon-tubiaozhizuo-",
    empty: "icon-empty",
    chat: "icon-liuyan",
};
export const types = Object.keys(classMap);
export default {
    props: {
        type:{
            type: String,
            required: true,
        }
    },
    computed: {
        fontClass() {
            return classMap[this.type];
        }
    }
}
</script>

<style scoped>
    @import "//at.alicdn.com/t/font_2594224_cgv1vpoa59u.css";
    .iconfont{
        color: inherit;
        font-size: inherit; 
    }
</style>