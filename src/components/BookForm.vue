<template>
  <div>
    <h3> Add your Book </h3>

   <form v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)" class="" action="#" method="post">
    <input type="text" name="title" value="" v-model="bookTitle" placeholder="Book Title">
    <input type="text" name="author" value="" v-model="bookAuthor" placeholder="Book Author">
    <button type="submit" name="button">Add Book</button>
</form>
   </div>
</template>

<script>
  export default {
    name: 'BookForm',
    props: ['books'],
    
    data(){
      return{
        bookTitle: '',
        bookAuthor: ''
      }
    },
    methods:{
      bookSubmit(bookTitle, bookAuthor){
        this.$emit('addBook', bookTitle, bookAuthor);
      }
    }
  }

</script>


<style scoped>


li{
display:block;
margin:0 10px;
}

</style>
