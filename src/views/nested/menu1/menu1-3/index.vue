<template>
  <div style="padding:30px;">
    <el-row style="padding:10px;">
      <el-button v-on:click="newyear">New Year's Day	Fri, Jan 1, 2021</el-button>
      <el-button v-on:click="lunar">Lunar New Year	Feb 11 – 17, 2021</el-button>
      <el-button v-on:click="qingming">Qingming Festival	Sun, Apr 4, 2021</el-button>
      <el-button v-on:click="labour">Labour Day	May 1 – 5, 2021</el-button>
      <el-button v-on:click="dragon">Dragon Boat Festival	Mon, Jun 14, 2021</el-button>
    </el-row>

    <el-row style="padding:10px;">
      <el-button v-on:click="autumn">Mid-Autumn Festival	Tue, Sep 21, 2021</el-button>
    </el-row>
  <el-card class="box-card"  style="padding:30px;" v-if="show">
  <div slot="header" class="clearfix">
    <span>Weather</span>
  </div>
  <div>
    {{weather}}
  </div>

</el-card>

  <el-card v-if="show" class="box-card"  style="padding:30px;">
  <div slot="header" class="clearfix">
    <span>Rental information</span>
  </div>
  <div>
    <div v-for="o in 4" :key="o" class="text item">
       {{'Address' + o }}
       {{' , Price: '}}
       {{rental+o}}
       {{'usd/day'}}
     </div>
  </div>

</el-card>
  </div>
</template>

<script>
export default {
  data () {
    return {
      weather : "wwe",
      rental:0,
      show: false
    }
  },
  methods:{
    newyear: function () {
      this.show = true;
      this.weather = "Breezy, 9°C";
      this.rental = 7;
    },
    lunar: function () {
      this.show = true;
      this.weather = "Sunny, 3°C";
      this.rental = 8;
    },
    qingming: function () {
      this.show = true;
      this.weather = "Windy, 9°C";
      this.rental = 9;
    },
    labour: function () {
      this.show = true;
      this.weather = "Rainy, 12°C";
      this.rental = 15;
    },
    dragon: function () {
      this.show = true;
      this.weather = "Breezy, 17°C";
      this.rental = 6;
    },
    autumn: function () {
      this.show = true;
      this.weather = "Sunny, 10°C";
      this.rental = 12;
    }
  }
}
</script>
