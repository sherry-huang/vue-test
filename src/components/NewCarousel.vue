<template>
  <a-carousel dots dots-class="slick-dots slick-thumb">
    <a slot="customPaging" slot-scope="props">
      <img :src="getImgUrl(props.i)" />
    </a>
    <div v-for="item in urlArr" :key="item">
      <img :src="item" />
    </div>
  </a-carousel>
</template>
<script>
import img from './cat-2.jpg'
const baseUrl1 = 'https://pic.pimg.tw/acatandcats/1344952155-375602234.jpg';
const baseUrl2 = img;
const baseUrl3 = 'https://4.bp.blogspot.com/-FI6LfVLyjWk/Xpq4MCak6MI/AAAAAAAADuU/_Cn5CV7xE9QUj5zT9EJcYTB4i1Ot4sdVQCLcBGAsYHQ/s1600/5cbc5e7c10abfdbb2c0edb6112de3234_s.jpg';
const baseUrl =
  'https://raw.githubusercontent.com/vueComponent/ant-design-vue/master/components/vc-slick/assets/img/react-slick/';

export default {
  data() {
    return {
      baseUrl,
      baseUrl1,
      baseUrl2,
      baseUrl3,
      urlArr: [baseUrl1, baseUrl2, baseUrl3]
    };
  },
  methods: {
    getImgUrl(i) {
      switch (i) {
        case 0:
          return baseUrl1
        case 1:
          return baseUrl2
        default:
          return baseUrl3
      }
    },
  },
};
</script>
<style scoped>
/* For demo */
.ant-carousel {
  text-align: center;
  height: 300px;
  line-height: 160px;
  background: #364d79;
  /* overflow: hidden; */
}
.ant-carousel >>> .slick-dots {
  height: auto;
}
.ant-carousel >>> .slick-slide img {
  /* border: 5px solid #fff; */
  display: block;
  margin: auto;
  max-width: 80%;
  height: 300px;
}
.ant-carousel >>> .slick-thumb {
  bottom: -45px;
}
.ant-carousel >>> .slick-thumb li {
  width: 60px;
  height: 45px;
}
.ant-carousel >>> .slick-thumb li img {
  width: 100%;
  height: 100%;
  filter: grayscale(100%);
}
.ant-carousel >>> .slick-thumb li.slick-active img {
  filter: grayscale(0%);
}
</style>
