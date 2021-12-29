<template>
  <div class="card-share">
    <div class="share-icons">
      <p>S H A R E</p>
      <ul>
        <li>
          <img :src="fb" alt="fb" />
        </li>
        <li><img :src="twitter" alt="twitter" /></li>
        <li>
          <img :src="pinterest" alt="pinterest" />
        </li>
      </ul>
    </div>
    <div class="share-logo">
      <button>
        <img :src="share_icon" alt="share" v-on:click="$emit('CardFooter')" />
      </button>
    </div>
  </div>
</template>
<script>
export default {
  name: "CardShare",
  data() {
    return {
      fb: require("/src/assets/icon-facebook.svg"),
      twitter: require("/src/assets/icon-twitter.svg"),
      pinterest: require("/src/assets/icon-pinterest.svg"),
      share_icon: require("/src/assets/icon-share.svg"),
    };
  },
};
</script>
<style scoped>
.card-share {
  display: flex;
  flex-direction: row;
  background-color: hsl(217, 19%, 35%);
  justify-content: space-between;
  padding: 1.3rem;
  align-items: center;
  transition: all 0.3s ease-in-out;
}
.share-icons {
  display: flex;
  flex-direction: row;
}
ul {
  display: flex;
  flex-direction: row;
  list-style: none;
  align-items: center;
}
p {
  color: hsl(212, 23%, 69%);
  padding: 8px 12px;
}
button {
  border: none;
  background-color: hsl(210, 46%, 95%);
  padding: 0.5rem;
  border-radius: 50%;
  cursor: pointer;
}
li {
  margin-left: 1rem;
}
</style>