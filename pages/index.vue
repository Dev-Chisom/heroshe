<template>
  <div class="min-h-screen bg-gray-200">
    <LoadingSpinner v-if="showHideSpinner" />
    <PageHeader :user="user" @showMobile="openMobile"/>
    <div
      class="min-h-screen flex overflow-hidden"
    >
      <Navigation class="hidden lg:block lg:w-64 xl:w-72 space-y-6" />
        
       <transition name="slide">
        <div v-if="mobile">
        <MobileNav class="w-screen md:w-full"/>
      </div>
      </transition>
      <main
        class="flex-1 bg-white m-0 lg:m-6 rounded-t-lg"
      >
        <Content :user="user" />
      </main>
    
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {},
      mobile: false,
       showHideSpinner: true
    };
  },
  async created() {
      this.showHideSpinner = true;
      await this.$axios
      .$get(process.env.API_URL)
      .then(response => {
        this.user = response;
        this.showHideSpinner = false;
      })
      .catch(error => console.log(error));
  },
  methods:{
    openMobile(){
      this.mobile = !this.mobile
    }
  },
};
</script>
<style scoped>
.slide-enter-active, .slide-leave-active {
  transition: width;
}
.slide-enter, .slide-leave-to{
  width:0;
}
</style>