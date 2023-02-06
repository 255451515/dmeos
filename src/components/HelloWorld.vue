<template>
   <div>
    <h1> {{ res }}</h1>
   </div>
</template>
<script>


 export default {
       name:"HelloWorld",
       data(){
        return {
          res:new Date().getDate()
        }
       },
  
 }
</script>