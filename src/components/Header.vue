/*
 * Created: 2020-04-27 08:55:03
 * Author : 黄雪梅
 * Last Modified: 2020-04-27 16:33:13
 * Modified By: 黄雪梅
 * Copyright (c) 2019. 深圳奥雅纳智能科技有限公司. All Rights Reserved.
 */

<template>
  <div class="header">
    <div class="df ac jsb container">
      <div class="df ac jc logo">
        <img src="./../assets/images/logo.png" />
      </div>
      <div class="df ac">
        <el-input class="input" size="small" v-model="searchVal" placeholder="搜索文章"></el-input>
        <div class="nav">
          <ul class="df ac" @click="navChange">
            <li class="nav-item">
              <a data-index="1" :class="activeIndex==1?'active':''">生物科学</a>
            </li>
            <li class="nav-item">
              <a data-index="2" :class="activeIndex==2?'active':''">自然科学</a>
            </li>
            <li class="nav-item">
              <a data-index="3" :class="activeIndex==3?'active':''">社会科学</a>
            </li>
            <li class="nav-item">
              <a data-index="4" :class="activeIndex==4?'active':''">毛泽东思想</a>
            </li>
          </ul>
        </div>
        <div class="management">
          <el-button type="primary" size="medium" icon="el-icon-edit">发布文章</el-button>
          <!-- <a>发布文章</a> -->
        </div>
        <div class="avator">
          <img src="./../assets/images/avator.png" />
        </div>
        <el-dropdown trigger="click">
          <span class="el-dropdown-link">
            黄雪梅
            <i class="el-icon-arrow-down el-icon--right"></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>退出账号</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      activeIndex: 1,
      searchVal: ""
    };
  },
  methods: {
    navChange(e) {
      let index = e.target.dataset.index || 1;
      if (index) {
        this.activeIndex = index;
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang='less'>
.header {
  height: 80px;
  position: fixed;
  left: 0;
  right: 0;
  background: #fff;
  border-bottom: 1px solid #dcdfe6;
  // box-shadow: 0px -2px 6px #888888;
  .container {
    width: 1150px;
    height: 100%;
    margin: auto;
    .logo {
      height: 100%;
      img {
        height: 50px;
      }
    }
    .nav {
      margin-right: 30px;
      li {
        a {
          display: block;
          height: 80px;
          line-height: 80px;
          position: relative;
          text-decoration: none;
          color: #8590a6;
          // opacity: 0.5;
          padding: 0 15px;
          cursor: pointer;
          &:hover {
            color: #1989fa;
          }
          &.active {
            color: #1989fa;
            &:after {
              content: "";
              display: inline-block;
              position: absolute;
              bottom: 0;
              left: 0;
              // left:calc(50% - 25%);
              width: 100%;
              height: 2px;
              background: #409eff;
            }
          }
        }
      }
    }
    .input {
      width: 200px;
      margin-right: 20px;
    }
    .avator {
      width: 60px;
      height: 60px;
      margin-right: 20px;
      // border-radius: 60px;
      // background: #f1f1f1;
      img {
        width: 100%;
        height: 100%;
      }
    }
    .management {
      margin-right: 30px;
      cursor: pointer;
      a {
        &:hover {
          color: #1989fa;
        }
      }
    }
  }
}
</style>
