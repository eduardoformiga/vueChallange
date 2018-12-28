<template>
  <div :class="cardState">
    <header>
      <slot name="header"></slot>
    </header>
    <main>
      <slot></slot>
      <MyButton title="Comprar" :state="cardState === 'promotion' ? 'block' : 'outline'"/>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<script>
import MyButton from "./MyButton.vue";

export default {
  name: "MyCard",
  components: {
    MyButton
  },
  props: {
    cardState: String
  }
};
</script>

<style scoped>
div {
  position: relative;
  margin: 10px;
  width: 170px;
  height: 330px;
  padding: 15px;
  border-radius: 2px;
  background-color: white;
  text-align: center;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  border-radius: 5px;
}

header {
  padding-bottom: 10px;
}

.promotion {
  border-top: 5px solid green;
}

.normal {
  border-top: 5px solid transparent;
}

footer {
  position: absolute;
  left: 0;
  bottom: 0;
  width: 93%;
  border-top: 1px solid #d8d7d7;
  padding: 7px;
}
</style>
