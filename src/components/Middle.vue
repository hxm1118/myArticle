/*
 * Created: 2020-04-27 14:27:05
 * Author : 黄雪梅
 * Last Modified: 2020-04-27 16:13:22
 * Modified By: 黄雪梅
 * Copyright (c) 2019. 深圳奥雅纳智能科技有限公司. All Rights Reserved.
 */

<template>
  <div class="f1 middle">
    <div class="article-item" v-for="(item,index) in articleData">
      <div class="df ac introduce">
        <img :src="item.src" />
        <div>
          <div class="title">{{item.name}}</div>
          <div class="text">
            {{item.text}}
            <a>阅读更多</a>
          </div>
        </div>
      </div>
      <div class="df ac actions">
        <div class="df ac actions-item">
          <img src="./../assets/images/middle-icon1.png" />
          <span>420 条评论</span>
        </div>
        <div class="df ac actions-item">
          <img src="./../assets/images/middle-icon2.png" />
          <span>分享</span>
        </div>
        <div class="df ac actions-item">
          <img src="./../assets/images/middle-icon3.png" />
          <span>收藏</span>
        </div>
        <div class="df ac actions-item">
          <img src="./../assets/images/middle-icon4.png" />
          <span>喜欢</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Middle",
  data() {
    return {
      articleData: [
        {
          name: "红楼梦",
          src: require("./../assets/images/红楼梦.jpg"),
          text:
            "《红楼梦》塑造了众多的人物形象，他们各自具有自己独特而鲜明的个性特征，成为不朽的艺术典型，在中国文学史和世界文学史上永远放射着奇光异彩。 《红楼梦》是一部具有高度思想性和高度艺术性的伟大作品，从《红楼梦》反映的思想倾向来看，作者具有初步的民主主义思想，他对现实社会包括宫廷及官场的黑暗，封建贵族阶级及其家庭的腐朽，封建的科举制度、婚姻制度、奴婢制度、等级制度..."
        },
        {
          name: "三国演义",
          src: require("./../assets/images/三国演义.jpg"),
          text:
            "《三国演义（套装上下册）》是罗贯中在民间传说和有关话本、戏曲的基础上改编而成的。作者通过集中描绘三国时代各封建统治集团之间的政治、军事、外交斗争，揭示了东汉末年社会的动荡和黑暗，谴责了封建统治者的暴虐，反映了民众的苦难和他们呼唤明君、呼唤安定的强烈愿望。 小说塑造了大量栩栩如生的人物，宽厚仁爱的刘备，残暴奸诈的曹操，一身正气的关羽，粗中有细的张飞..."
        },
        {
          name: "水浒传",
          src: require("./../assets/images/水浒传.jpg"),
          text:
            "《水浒传》是一部长篇英雄传奇，是中国古代长篇小说的代表作之一，是以宋江起义故事为线索创作出来的。宋江起义发生在北宋徽宗时期，《宋史》的《徽宗本纪》、《侯蒙传》、《张叔夜传》等都有记载。从南宋起，宋江起义的故事就在民间流传，《醉翁谈录》记载了一些独立的有关水浒英雄的传说，《大宋宣和遗事》把许多水浒故事联缀起来，和长篇小说已经很接近。元代出现了不少水浒戏..."
        },
        {
          name: "西游记",
          src: require("./../assets/images/西游记.jpg"),
          text:
            "《西游记》主要描写的是孙悟空保唐僧西天取经，历经九九八十一难的故事。唐僧取经是历史上一件真实的事。大约距今一千三百多年前，即唐太宗贞观元年（627），年仅25岁的青年和尚玄奘离开京城长安，只身到天竺（印度）游学。他从长安出发后，途经中亚、阿富汗、巴基斯坦，历尽艰难险阻，到达了印度。他在那里学习了两年多，并在一次大型佛教经学辩论会任主讲..."
        }
      ]
    };
  }
};
</script>

<style scoped lang='less'>
.middle {
  padding: 50px 0;
  margin-right: 80px;

  .article-item {
    margin-bottom: 40px;
    .introduce {
      img {
        width: 160px;
      }
      .title {
        font-size: 16px;
        margin-bottom: 10px;
        font-weight: bold;
      }
      .text {
        line-height: 30px;
        a {
          color: #1989fa;
          cursor: pointer;
        }
      }
    }
    .actions {
      margin-left: 160px;
      margin-top: 20px;
      cursor: pointer;
      .actions-item {
        margin-right: 20px;
        img {
          width: 20px;
          margin-right:5px;
        }
        span {
          color: #8590a6;
        }
      }
    }
  }
}
</style>