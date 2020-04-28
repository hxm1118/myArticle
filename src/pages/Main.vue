/*
 * Created: 2020-04-27 10:47:57
 * Author : 黄雪梅
 * Last Modified: 2020-04-27 16:09:56
 * Modified By: 黄雪梅
 * Copyright (c) 2019. 深圳奥雅纳智能科技有限公司. All Rights Reserved.
 */
 <template>
  <div class="main">
    <Header></Header>
    <div class="container">
      <div class="df content">
        <Middle></Middle>
        <SideBar></SideBar>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./../components/Header";
import SideBar from "./../components/SideBar";
import Middle from "./../components/Middle";
export default {
  name: "Main",
  components: { Header, SideBar,Middle },
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang='less'>

.container {
  padding-top:80px;
  .content {
    width: 1150px;
    margin: auto;
    overflow: hidden;
    box-sizing: border-box;
  }
}
</style>


