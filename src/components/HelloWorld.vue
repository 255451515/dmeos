<template>
   <div id="huang">
    <div>
      <p>重庆专升本考试时间:<span><b>{{ ress }}</b></span></p>
      <p>少壮不努力,老大徒伤悲</p>
      <h1>考试剩余时间:{{ get() }}月</h1>
      <div>努力奋斗还剩<span>{{etss() }}</span> 天</div>
      
    </div>
     <!-- <button  id="hang" v-on:click="hangs">切换主题</button> -->
   </div>
</template>
<script>



 export default {
       name:"HelloWorld",
       data(){
        return {
           ress:"2023-4-8",
          res:new Date().getUTCMonth()+1,
          ret: false,
          resss:new Date("May 7, 2023 23:15:00").getUTCMonth(),
          rets:new Date("April 7, 2023 23:15:00")
        }
       },
       methods:{
         get(){
           return this.resss-this.res
         },
         etss(){
          var endTime = new Date(this.rets);
            var startTime = new Date();
            var times = parseInt( ( endTime.getTime() - startTime.getTime() ) / 1000 );
            var day = parseInt(times / (24*60*60));
            // var house =  parseInt( (times % (24*60*60)) / (60*60) );
            // var minute = parseInt( (times % (60*60)) / (60) );
            // var second = times % 60;
 
 return          day

        },
        // hangs(){
        //    this.$nextTick(function(){
        //     document.body.classList.toggle("backger")
        //   document.querySelector("button").classList.toggle("backger")
        //    })
           
        // }
       }
  
 }
</script>
<style scoped>
    span{
      text-shadow: 1px 1px 2px red, 0 0 1px blue, 0 0 0.2px blue;
      font-size: 20px;
    }
    #huang{
      position: relative;
    }
     #hang{
      position: absolute;
      top: 20px;
    left: 24px;
     }
     .backger{
       background: rgba(red, green, blue, alpha) !important
     }
</style>