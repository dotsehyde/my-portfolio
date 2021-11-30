<template>
  <div id="work">
    <div class="heading">{{ text }}</div>
    <WorkCard title="AgriWatch" image="../assets/wor.png" />
    <WorkCard title="Wookin Shopping" image="../assets/wor.png" />
    <WorkCard title="Wookin Shopping" image="../assets/wor.png" />
    <WorkCard title="Wookin Shopping" image="../assets/wor.png" />
  </div>
</template>

<script>
import WorkCard from "./WorkCard.vue";
export default {
  components: { WorkCard },
  name: "works",
  data() {
    return {
      text: "=: My Works {}",
    };
  },
};
</script>

<style lang="scss" scoped>
#work {
  padding: 25px 150px;
  background: #edf7fa;
  box-shadow: 0px 4px 10px rgba(187, 225, 250, 0.25);
  margin-top: 10px;
  @media (max-width: 768px) {
    text-align: center;
    padding: 0 20px;
  }
  .heading {
    color: #21243d;
    font-weight: bold;
    font-size: 40px;
    padding: 20px 0px;
    @media (max-width: 768px) {
      padding: 5px 0;
      text-align: center;
      font-size: 30px;
    }
  }
}
</style>
