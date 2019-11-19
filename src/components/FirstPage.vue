<template>
  <section class="search-sec">
    <div class="container">
      <Header style="margin-top:5%:"></Header>
      <form action="#" method="post" novalidate="novalidate">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-3 col-md-3 col-sm-12 p-0">
                <v-select :items="items" label="choose your options" solo></v-select>
              </div>
              <div class="col-lg-3 col-md-3 col-sm-12 p-0">
                <!-- <div class="form-control search-slt"> -->
                <input type="text" class="datepicker" placeholder="location" />
                <!-- </div>                            -->
              </div>
              <div class="col-lg-3 col-md-3 col-sm-12 p-0">
                <div class="form-control search-slt">
                  <input type="date" v-model="date" />
                </div>
              </div>
              <div class="col-lg-3 col-md-3 col-sm-12 p-0">
                <button type="button" class="btn btn-primary wrn-btn" @click="search()">Search</button>
              </div>
            </div>
          </div>
        </div>
      </form>
    </div>
  </section>
  <!-- <Header></Header> -->
</template>
<style scoped>
.search-sec {
  padding: 2rem;
}
.search-slt {
  display: block;
  width: 100%;
  font-size: 0.875rem;
  line-height: 1.5;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  height: calc(3rem + 2px) !important;
  border-radius: 0;
  font-family: Raleway-SemiBold;
}
.wrn-btn {
  width: 100%;
  font-size: 16px;
  font-weight: 400;
  text-transform: capitalize;
  height: calc(3rem + 2px) !important;
  border-radius: 0;
  font-family: Raleway-SemiBold;
}
.datepicker {
  width: 100%;
  font-size: 16px;
  font-weight: 400;
  text-transform: capitalize;
  height: calc(3rem + 2px) !important;
  border-radius: 0;
  font-family: Raleway-SemiBold;
}
.container {
  max-width: 1140px;
  margin-top: 270px;
}
option {
  font-family: Raleway-SemiBold;
}
.col-lg-3 {
  -ms-flex: 0 0 25%;
  -webkit-box-flex: 0;
  flex: 0 0 25%;
  max-width: 25%;
  border: 2px solid;
  border-color: #1976d2;
  /* border-radius: 10px;  */
}
</style>
<script>
import Header from "../components/Header.vue"
export default {
  components:{
    Header
  },
  props: [],
  mounted() {},
  data() {
    return {
      // date: new Date().toJSON.split('T')[0],
      items: ["car", "van", "bus", "m otorcycle", "boat"],
      date: new Date()
    };
  },
  methods: {
    search() {
      this.$router.push("/mainpage");
    }
  }
};
</script>