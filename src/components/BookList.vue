<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <ul>
        <li v-for="book in books">{{book.title}}:{{book.author}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'BookList',
  data() {
    return {
      title: 'All Books',
      books:[
        {title:'Self-Reliance', author:'Ralph'},
        {title:'Self-Reliance2', author:'Hari'},
        {title:'Self-Reliance3', author:'Linta'},
      ]
    };
  },
};
</script>


<style scoped>
h1, h2 {
  font-weight: normal;
}

ul{
  list-style-type:normal;
  padding:0;
}
li{
display:block;
margin:0 10px;
}

</style>
