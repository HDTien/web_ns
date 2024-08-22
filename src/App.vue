<template>
<div class="container">
  <!-- <DangNhap></DangNhap> -->
<TheHeader></TheHeader>
<TheMenu></TheMenu>
<TheMain></TheMain>
</div>
</template>

<script>
import TheHeader from './layouts/TheHeader.vue';
import TheMain from './layouts/TheMain.vue';
import TheMenu from './layouts/TheMenu.vue';
// import DangNhap from './layouts/DangNhap.vue';
export default {
  name: 'App',
  components: {
    TheHeader,TheMain,TheMenu,
  }
}
</script>

<style>
@import url(main.css);
</style>
