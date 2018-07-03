<template>
    <div class='item'>
      <nuxt-link :to="'path/'+item.id">
        <h1>{{item.id}}</h1>

      </nuxt-link>
      <div>
          {{item.gender}}
      </div>
      <p>{{item.email}}</p>
    </div>
</template>


<script>
  export default {
    props: {
      itemData:{
        type: Object
      },
    },
    data(){
      return{
        item: this.itemData
      }
    }
  }
</script>

<style>
  .item {
    padding: 20px;
    background-color: lightskyblue;
  }
</style>
