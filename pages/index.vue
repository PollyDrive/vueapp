<template>
  <section class="container">
    <div>
      <app-logo/>
      <h1 class="title">
        vueapp
      </h1>
      <div class="grid">
        <div v-for="item in dataList" :key="item.id">
          <Item :itemData = 'item'/>

        </div>
      </div>
    </div>
  </section>
</template>

<script>
import myData from '../data/MOCK_DATA.json';
import Item from '@/components/Item.vue';

export default {
  components: {
    Item
  },
  data(){
    return{
      dataList: myData
    }
  }
}
</script>

<style>
  .grid{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 20px;
  }
</style>


