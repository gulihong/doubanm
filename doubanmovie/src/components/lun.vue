<template lang="html">
<<<<<<< HEAD

</template>

<script>
let jsonp = require('jsonp')
export default {
  name: 'ping',
  data() {
    return { // 在数据中接收
      num: this.$route.params.id,
      msg: {}
    }
  },
  methods: {
    getImage(url) {
      if (url !== undefined) {
        return url.replace('http://', 'https://images.weserv.nl/?url=');
      }
    },
    getData() {
        jsonp("https://api.douban.com/v2/movie/subject/" + this.num + "/reviews?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=20&client=something&udid=dddddddddddddddddddddd", null, (err, data) => {
        if (err) {
          console.error(err);
        } else {
          console.log(data);
        }
      })
    }
  },
  created() {
    this.getData();
  },
  updated() {

  }
}
</script>
<style lang="css">

=======
  <div class="lun">
   <h1><span>话题</span><label>写话题</label></h1>
   <ul>
     <li>今天有部分影评人在推特上发影评了</li>
     <li><img src="../../static/img/li1.jpg" alt=""><label>blacket</label><span>7分钟前更新</span></li>
     <li>就问你一句话？这片子为什么整天翻拍</li>
     <li><img src="../../static/img/li2.jpg" alt=""><label>沉思.大海</label><span>12分钟前更新</span></li>
     <li>你们看的是国语版还是原版？</li>
     <li><img src="../../static/img/li3.jpg" alt=""><label>橘子.汽水</label><span>14分钟前更新</span></li>
     <li>那个评论者小绿是个什么鬼</li>
     <li><img src="../../static/img/li4.jpg" alt=""><label>谁是小绿</label><span>18分钟前更新</span></li>
     <li>我的热情就像一把火。。。</li>
     <li><img src="../../static/img/fire.png" alt=""><label>火火</label><span>20分钟前更新</span></li>
     <li class="lastli">全部话题9条</li>
   </ul>
  </div>
</template>

<script>
export default {
  name: "ping"
};
</script>
<style lang="css" scoped>
.lun ul {
  list-style: none;
}
.lun h1 {
  width: 90%;
  height: 0.9rem;
  line-height: 0.9rem;
  color: #000;
  margin: 0 auto;
  font-size: 0.3rem;
}
.lun h1 label {
  float: right;
  margin-top: 0.2rem;
  font-size: 0.15rem;
  text-align: center;
  color: green;
  width: 0.8rem;
  height: 0.4rem;
  line-height: 0.4rem;
  border: 0.01rem solid green;
  border-radius: 0.04rem;
}
.lun ul > li {
  line-height: 0.7rem;
  font-weight: 900;
  font-size: 0.25rem;
}
.lun ul {
  width: 90%;
  margin: 0 auto;
}
.lun li img {
  width: 0.35rem;
  height: 0.35rem;
  vertical-align: text-bottom;
  margin-right: 0.02rem;
}
.lun ul li span,
.lun ul li label {
  font-weight: normal;
  font-size: 0.2rem;
  color: gray;
}
.lun ul li span {
  float: right;
}
.lastli {
  text-align: center;
  color: green;
  font-size: 0.2rem;
  font-weight: normal;
}
>>>>>>> df5c1edf4c444ef0c4d6904ad0657008a563b981
</style>
