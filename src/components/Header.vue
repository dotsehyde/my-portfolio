<template>
  <div class="row">
    <div class="col">
      <router-link to="profile" smooth="{true}">
        <a>Profile</a>
      </router-link>
    </div>
    <div class="col">
      <router-link to="work" smooth="{true}">
        <a>Works</a>
      </router-link>
    </div>
    <div class="col">
      <router-link to="hire" smooth="{true}">
        <a href="/">Hire Me</a>
      </router-link>
    </div>
  </div>
</template>
<script>
export default {
  name: "header",
};
</script>
<style lang="scss" scoped>
.row {
  display: flex;
  margin-top: 10px;
  position: sticky;
  top: 0;
  z-index: 10;
  justify-content: flex-end;
  @media (max-width: 768px) {
    justify-content: center;
  }
}

.col {
  margin: 10px 15px;
}
a {
  text-decoration: none;
  color: black;
  cursor: pointer;
  font-size: 1.3rem;
  &:hover {
    color: #00a8cc;
  }
  @media (max-width: 768px) {
    font-size: 1rem;
  }
}
</style>
