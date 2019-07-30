<template>
   <li>{{book.title}}:{{book.author}}</li>
</template>

<script>

  export default {
    name: 'BookItems',
    props: [book]
  
    
  }


</script>


<style scoped>


li{
display:block;
margin:0 10px;
}

</style>
