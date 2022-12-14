<template>
  <div class="Single_Page_container">
   <div class="book-item">   
  <div class="img" >
    <img :alt="title" :src="src"/>
 </div>

<div class="Book-Details">
 <h3>{{title}}</h3>
  <p>Description: {{description}}</p>
  <p>Book Status :{{status}}</p>
  <p>Book Price :{{price}}</p> 
  </div>
  </div>
    </div>
</template>

<script>
export default {
props:['id'],
computed:{
    title(){
        return this.$route.query.title;
    },
    description(){
        return this.$route.query.description;
    },
      src(){
        return this.$route.query.src;
    },
    status(){
        return this.$route.query.status;

    },
   price(){
    return this.$route.query.price;
   },

},
}
</script>

<style scoped>

.book-item{
  display: flex;
  align-items: center;
}

.img{
  margin:0 100px;
}

@media (max-width:600px) {
 .book-item{
 display: flex;
 flex-direction: column;
} 
}
</style>