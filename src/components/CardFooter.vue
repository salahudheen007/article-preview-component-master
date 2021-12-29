<template>
  <div class="avatar">
    <div class="avatar-image">
      <img
        :src="avatar_image"
        class="avatar-img"
        alt="avatar"
      />
    </div>
    <div class="avatar-name">
      <h5>Michelle Appleton</h5>
      <p>28 Jun 2020</p>
    </div>
    <div class="avatar-share">
      <button><img :src="share_icon" alt="share" v-on:click="$emit('CardShare')" /></button>
    </div>
  </div>
</template>
<script>
export default {
  name: "CardFooter",
  data(){
    return{
      avatar_image:require("/src/assets/avatar-michelle.jpg"),
      share_icon:require("/src/assets/icon-share.svg")
    }
  }
};
</script>
<style scoped>
.avatar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: row;
  background-color: white;
  padding: 0 2rem 1.5rem 2rem;
 transition: all .3s ease-in-out;
}
.avatar-img{
    width: 50px;
    border-radius: 50%;
}
h5{
    color: hsl(217, 19%, 35%);
    line-height: 1.5rem;
}
p{
    color: hsl(212, 23%, 69%);
}
button{
    border: none;
    background-color:hsl(210, 46%, 95%);
    padding: .5rem;
    border-radius: 50%;
  cursor: pointer;

}
</style>