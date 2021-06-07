<template>
  <div>
    <Pager
      :total="total"
      :current="current"
      @pageChange="handlePageChange($event)"
    />
  </div>
</template>

<script>
import Pager from './';

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
    Pager
  }
}
</script>



