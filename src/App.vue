<template>
  <div>
    <Avatar url="http://mdrs.yuanjin.tech/FgMwAPYq17So9nwVH44ltDHo7u3c" :size="100" />
    <Icon type="home"/>
    <Pager
      :total="total"
      :current="current"
      @pageChange="handlePageChange($event)"
    />
  </div>
</template>

<script>
import Avatar from './components/Avatar';
import Icon from './components/Icon.vue';
import Pager from './components/Pager.vue';

export default{
  data() {
    return {
      current: 1,
      total: 302,
    };
  },
  methods: {
      handlePageChange(newPage) {
        this.current = newPage;
        console.log("加载当前页数据");
      },
  },
  name:"App",
  components:{
    Avatar,
    Icon,
    Pager
  }
}
</script>

<style scoped>
.iconfont {
  font-size: 26px;
  color: red;
}
</style>


