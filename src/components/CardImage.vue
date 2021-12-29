<template>
    <div>
        <img :src="image" alt="">
    </div>
</template>
<script>
export default {
    name:'CardImage',
    data(){
        return{
            image:require("/src/assets/drawers.jpg" )
        }
    }
}
</script>
<style scoped>

  div{
       overflow: hidden;
  }
@media (max-width:720px){
     div{
     height: 13rem;
 }
  img{
     width: 100%;
    
 }
}
@media(min-width:721px){
    div{
        height: 18rem;
        width: 50rem;
    }img{
         height: 100%;
    }
}
</style>