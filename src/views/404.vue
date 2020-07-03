<template>
  <div class="main">
    <div class="bg">
      <!-- <p>{{time}}</p> -->
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
        time:5
    };
  },
  mounted() {
    setTimeout(() => {
      this.$router.push("/");
    }, 5000);
  },
   watch:{
    'time':function(newVal,oldVal){
          if(newVal==0){
            this.$router.push('/');
          }
    }
  }
};
</script>
<style lang="scss" scoped>
.main {
  .bg {
    width: 100%;
    height: 100vh;
    background-repeat: no-repeat;
    background: url(
      https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=2443868858,332759847&fm=26&gp=0.jpg
    );
    background-size: cover;
  }
}
</style>