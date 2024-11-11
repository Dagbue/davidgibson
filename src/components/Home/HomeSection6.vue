<template>
  <div class="alpha">

    <button  class="btn-default-2" >VIEW ALL POSTS</button>
    <button @click="onPostClick" class="btn-default" >VIEW ALL POSTS</button>
  </div>
</template>

<script>
export default {
  name: "HomeSection6",
  methods: {
    onPostClick() {
      this.$router.push("/feeds");
      window.scrollTo(0, 0);
    },
  },
}
</script>

<style scoped>
.alpha{
  display: flex;
  flex-direction: row;
  background: rgba(0, 0, 0, 0.02);
  width: 73%;
  margin-right: auto;
  margin-left: auto;
  margin-top: 5%;
  margin-bottom: 5%;
}

.btn-default{
  background-color: #333;
  border: none;
  color: #FFFFFF;
  opacity: 1;
  width: 50%;
  text-align: center;
  padding-top: 20px;
  padding-bottom: 18px;
  border-radius: 0 6px 6px 0;
}

.btn-default-2{
  background-color: rgba(0, 0, 0, 0.02);
  border: none;
  color: rgba(0, 0, 0, 0.02);
  opacity: 1;
  width: 50%;
  text-align: center;
  padding-top: 20px;
  padding-bottom: 18px;
  border-radius: 6px 0 6px 0;
}

@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .alpha{
    width: 93%;
  }
}

@media (max-width: 500px) {

}
</style>