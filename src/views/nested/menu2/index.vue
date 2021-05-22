<template>
  <div style="padding:30px;">
    <el-row style="padding:10px;">
      <el-button v-on:click="newyear">New Year's Day	Fri, Jan 1, 2021</el-button>
      <el-button v-on:click="lunar">Martin Luther King Jr. Day	Mon, Jan 18, 2021</el-button>
      <el-button v-on:click="labour">Independence Day	Mon, Jul 5, 2021</el-button>
      <el-button v-on:click="dragon">Labor Day	Mon, Sep 6, 2021</el-button>
      <el-button v-on:click="qingming">Thanksgiving	Thu, Nov 25, 2021</el-button>
    </el-row>

    <el-row style="padding:10px;">
      <el-button v-on:click="autumn">Christmas Day	Fri, Dec 24, 2021</el-button>
    </el-row>
<!--  <el-card class="box-card"  style="padding:30px;" v-if="show">
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

</el-card> -->
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
      this.weather = "Sunny, 5°C";
      this.rental = 5;
    },
    lunar: function () {
      this.show = true;
      this.weather = "Snow, -3°C";
      this.rental = 7;
    },
    qingming: function () {
      this.show = true;
      this.weather = "Windy, 7°C";
      this.rental = 3;
    },
    labour: function () {
      this.show = true;
      this.weather = "Rainy, 15°C";
      this.rental = 8;
    },
    dragon: function () {
      this.show = true;
      this.weather = "Breezy, 19°C";
      this.rental = 1;
    },
    autumn: function () {
      this.show = true;
      this.weather = "Sunny, 12°C";
      this.rental = 9;
    }
  }
}
</script>
