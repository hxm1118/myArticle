/*
 * Created: 2020-04-27 10:42:30
 * Author : 黄雪梅
 * Last Modified: 2020-04-27 16:06:10
 * Modified By: 黄雪梅
 * Copyright (c) 2019. 深圳奥雅纳智能科技有限公司. All Rights Reserved.
 */

<template>
  <!-- <el-scrollbar class="scrollbar" :native="false"> -->
    <div class="sideBar">
      <div v-for="(item,index) in sideBarData" :key="index">
        <div class="bar-title">{{item.title}}</div>
        <ul>
          <li class="bar-item" v-for="(myitm,myidx) in item.data" :key="myidx" @click="barChange(index,myidx)">
            <a :class="myitm.active?'active':''">{{myitm.name}}</a>
          </li>
        </ul>
      </div>
    </div>
  <!-- </el-scrollbar> -->
</template>

<script>
export default {
  name: "SideBar",
  data() {
    return {
      sideBarData: [
        {
          title: "小说",
          data: [
            {
              active: false,
              name: "中国当代小说"
            },
            {
              active: false,
              name: "中国古典小说"
            },
            {
              active: false,
              name: "影视小说"
            },
            {
              active: false,
              name: "四大名著"
            },
            {
              active: false,
              name: "中国历史"
            },
            {
              active: false,
              name: "魔幻/奇幻/玄幻"
            }
          ]
        },
        {
          title: "书法",
          data: [
            {
              active: false,
              name: "书法赏析"
            },
            {
              active: false,
              name: "技法/教程"
            },
            {
              active: false,
              name: "书法理论"
            },
            {
              active: false,
              name: "硬笔书法"
            }
          ]
        },
        {
          title: "励志与成功",
          data: [
            {
              active: false,
              name: "经典著作"
            },
            {
              active: false,
              name: "文明礼仪"
            },
            {
              active: false,
              name: "智慧格言"
            },
            {
              active: false,
              name: "人际与社交"
            }
          ]
        }
      ]
    };
  },
  methods:{
      barChange(index1,index2){
          this.sideBarData.forEach((item,index)=>{
              item.data.forEach((itm,idx)=>{
                  if(index1==index&&index2==idx){
                      itm.active=true
                  }else{
                      itm.active=false
                  }
              })
          })
      }
  }
};
</script>

<style scoped lang='less'>
//滚动条样式更改
// .scrollbar {
//   width: 240px;
//   height: 100%;
//   /deep/.el-scrollbar__wrap {
//     overflow-x: hidden;
//   }
// }
.sideBar {
  width: 200px;
  height: 100%;
  padding: 40px 0;
  .bar-title {
    font-size: 16px;
    color: #333;
    line-height: 40px;
    height: 40px;
    font-weight: bold;
  }
  .bar-item {
    a {
      display: block;
      height: 40px;
      color: #444;
      line-height: 40px;
      cursor: pointer;
      &:hover {
        color: #1989fa;
      }
      &.active{
          color: #1989fa;
      }
    }
  }
}
</style>
