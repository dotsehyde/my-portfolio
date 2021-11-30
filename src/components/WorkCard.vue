<template>
  <div class="wrapper">
    <img class="image" :alt="title" src="../assets/wor.png" />

    <div :style="{ marginLeft: '20px' }">
      <p class="title">{{ title }}</p>
      <div class="innerRow">
        <div class="dateCtn">2020</div>
        <div class="v-divider"></div>
        <p class="cat">Website</p>
      </div>
      <p class="desc">
        Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet
        sint. Velit officia consequat duis enim velit mollit. Exercitation
        veniam consequat sunt nostrud amet.
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "workcard",
  props: {
    title: String,
    image: String,
  },
});
</script>

<style lang="scss" scoped>
.wrapper {
  margin-top: 50px;
  display: flex;
  justify-content: start;
  align-items: center;
  @media (max-width: 768px) {
    flex-direction: column;
  }
}
.v-divider {
  border: 1px solid #bebebe;
  height: 25px;
  margin: 0 15px;
  align-self: stretch;
}
.image {
  border-radius: 6px;
  width: 246px;
  height: 180px;

  @media (max-width: 428px) {
    width: 350px;
    height: 250px;
  }
  @media (max-width: 375px) {
    width: 300px;
    height: 200px;
  }
}
.innerRow {
  display: flex;
  justify-content: start;
  @media (max-width: 768px) {
    justify-content: center;
  }
  @media (max-width: 428px) {
    justify-content: flex-start;
  }
  @media (max-width: 375px) {
    justify-content: center;
  }
}
.title {
  font-weight: bold;
  font-size: 30px;
  /* line-height: 44px; */
  color: var(--black);
  @media (max-width: 768px) {
    text-align: center;
    padding: 5px 0;
  }
  @media (max-width: 428px) {
    text-align: left;
    padding: 5px 0;
  }
  @media (max-width: 375px) {
    text-align: center;
    padding: 5px 0;
  }
}
.cat {
  font-size: 20px;
  /* line-height: 29px; */
  color: #8695a4;
}
.dateCtn {
  background: var(--black);
  border-radius: 16px;
  width: 62px;
  height: 25px;
  color: white;
  align-items: center;
  display: flex;
  justify-content: center;
}
.desc {
  font-size: 16px;
  /* line-height: 23px; */
  color: var(--black);
  @media (max-width: 768px) {
    justify-content: center;
    padding: 5px 15px;
  }
  @media (max-width: 428px) {
    text-align: center;
    padding: 5px 0;
  }
  @media (max-width: 375px) {
    text-align: center;
    padding: 5px 0;
  }
}
</style>
