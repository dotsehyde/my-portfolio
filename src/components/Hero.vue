<template>
  <div class="ctn">
    <div class="textCtn">
      <p class="title">
        {{ txt }}
        <br />
        I'm Benjamin Dotse;
      </p>
      <p class="subtitle">
        A <b>software developer</b> with over 3 years of experience and strong
        knowledge in web and mobile development.
        <br />
        I have been passionate about computer programming since I was 15 years
        old.
        <br />
        As a freelancer, I successfully developed web apps and cross-platform
        mobile apps for clients.
      </p>
      <div class="btn">Download Resume:</div>
    </div>
    <div class="imgCtn">
      <img alt="picture" src="../assets/pic.jpg" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      txt: "{{ Hello World }}",
    };
  },
};
</script>

<style lang="scss" scoped>
.ctn {
  display: flex;
  justify-content: space-around;
  padding: 50px 150px;
  @media (max-width: 992px) {
    flex-direction: column;
    padding: 8px 10px;
  }
}
.textCtn {
  flex: 2;
  padding-top: 10px;
  @media (max-width: 992px) {
    order: 2;
    display: flex;
    padding: 0 30px;
    flex-direction: column;
    align-items: center;
  }
}
.imgCtn {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  @media (max-width: 992px) {
    order: 1;
  }
}
.btn {
  background: #ff6464;
  border-radius: 5px;
  font-weight: 500;
  font-size: 20px;
  color: #ffffff;
  padding: 8px;
  margin: 8px 0px;
  cursor: pointer;
  text-align: center;
  width: 208px;
  &:hover {
    margin: 8px 0px;

    color: #21243d;
    background: #fff;
    border: 0.2px #ff6464 solid;
  }
  @media (max-width: 768px) {
    order: 3;
  }
}
.title {
  font-style: normal;
  font-weight: bold;
  font-size: 44px;
  color: #21243d;
  line-height: 65px;
  @media (max-width: 992px) {
    text-align: center;
    font-size: 34px;
    line-height: 45px;
  }
}
.subtitle {
  font-style: normal;
  font-weight: 300;
  font-size: 17px;
  padding-right: 50px;
  line-height: 23px;
  color: #21243d;
  @media (max-width: 992px) {
    text-align: center;
    padding-right: 0px;
  }
}
img {
  height: 300px;
  width: 300px;
  border-radius: 50%;
  @media (max-width: 992px) {
    height: 243px;
    width: 243px;
  }
}
</style>
