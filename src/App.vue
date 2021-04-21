<template>
  <div id="app">
    <Header @showModal="showModal" />
    <Main></Main>
    <Footer></Footer>

     <Modal
        v-if="isVisibleModal"
        @closeModal="showModal"
    />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Modal from "@/components/Modal";
import Main from "@/components/Main";
import Footer from "@/components/Footer";
export default {
  name: 'App',
  data(){
    return{
      isVisibleModal: false
    }
  },
  components: {
    Header,
    Modal,
    Main,
    Footer
  },
  methods:{
    showModal(){
      this.isVisibleModal = !this.isVisibleModal
    }
  },
  watch:{
    isVisibleModal: function (){
      if(this.isVisibleModal){
        console.log('rtsd')
        document.documentElement.style.overflow = 'hidden'
      }else{
        document.documentElement.style.overflow = 'auto'
      }
    }
  }
}
</script>

<style lang="scss">
#app{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
