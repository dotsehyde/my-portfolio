<template>
  <div class="wrapper">
    <p class="title">{{ title }}</p>
    <p class="loc">- {{ loc }}</p>
    <div class="subCtn">
      <p class="cert">{{ cert }}</p>
      <div class="v-divider" />
      <p class="date">{{ date }}</p>
    </div>
    <div class="h-divider" />
  </div>
</template>
<script>
export default {
  name: "educard",
  props: {
    title: String,
    loc: String,
    cert: String,
    date: String,
  },
};
</script>
<style lang="scss" scoped>
.wrapper {
  padding: 0 150px;
  margin-top: 50px;
  @media (max-width: 768px) {
    padding: 0 50px;
  }
}
.title {
  font-weight: 500;
  font-size: 25px;
  line-height: 25px;
  color: car(--black);
  @media (max-width: 768px) {
    line-height: 30px;
  }
}

.v-divider {
  border: 1px solid #bebebe;
  height: 25px;
  margin: 0 15px;
  align-self: stretch;
}

.subCtn {
  display: flex;
  justify-content: start;
}

.cert {
  font-size: 18px;
  color: #21243d;
}

.date {
  font-size: 18px;
  color: #8695a4;
  font-style: italic;
}
.loc {
  font-size: 15px;
  color: #8695a4;
  line-height: 30px;
  font-style: italic;
}
.h-divider {
  height: 0px;

  margin-top: 5px;
  border: 1px solid #e0e0e0;
}
</style>
