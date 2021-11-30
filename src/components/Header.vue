<template>
  <div class="row">
    <h4>{{ logo }}</h4>
    <div>
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
  </div>
</template>
<script>
export default {
  name: "app-header",
  data() {
    return {
      logo: "<Benjamin. />",
    };
  },
};
</script>
<style lang="scss" scoped>
h4 {
  color: black;
  cursor: pointer;
  font-size: 1.7rem;
  @media (max-width: 768px) {
    font-size: 1.5rem;
  }
}
.row {
  padding: 10px 120px;
  background-color: var(--primaryColor);
  display: flex;
  /* margin-top: 0px; */
  position: sticky;
  top: 0;
  z-index: 10;
  justify-content: space-between;
  align-items: center;
  @media (max-width: 768px) {
    justify-content: center;
    flex-direction: column;
    padding: 10px 20px;
  }
}

.col {
  margin: 10px 15px;
  display: inline;
  @media (max-width: 768px) {
    margin: 8px 10px;
  }
}
a {
  text-decoration: none;
  color: black;
  cursor: pointer;
  font-size: 1.3rem;
  transition: 0.3s color ease;
  &:hover {
    color: var(--black);
  }
  @media (max-width: 768px) {
    font-size: 1rem;
  }
}
</style>
