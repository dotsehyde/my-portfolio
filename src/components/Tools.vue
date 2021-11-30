<template>
  <div class="ctn">
    <div class="headCtn">
      <h4>{{ langText }}</h4>
    </div>
    <div class="langCtn">
      <div class="lang" v-for="i in icons" :key="i.alt">
        <a :href="i.link" target="_blank">
          <img :src="i.icon" :alt="i.alt" height="50" width="50"
        /></a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "tools",
  data() {
    return {
      langText: "[ Languages and Frameworks ]",
      icons: [
        {
          icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg",
          alt: "html5",
          link: "https://www.w3.org/html/",
        },
        {
          icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg",
          alt: "css3",
          link: "https://www.w3schools.com/css/",
        },
        {
          icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg",
          alt: "javascript",
          link: "https://developer.mozilla.org/en-US/docs/Web/JavaScript",
        },
        {
          icon: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/dart/dart.png",
          alt: "dart",
          link: "https://www.dart.dev/",
        },
        {
          icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg",
          alt: "python",
          link: "https://www.python.org",
        },
        {
          icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg",
          alt: "reactjs",
          link: "https://reactjs.org/",
        },
        {
          icon: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/flutter/flutter.png",
          alt: "flutter",
          link: "https://flutter.dev",
        },
        {
          icon: "https://img.icons8.com/color/48/000000/vue-js.png",
          alt: "vuejs",
          link: "https://vuejs.org/",
        },
        {
          icon: "https://img.icons8.com/color/48/000000/material-ui.png",
          alt: "material-ui",
          link: "https://mui.com",
        },
        {
          icon: "https://seeklogo.com/images/A/ant-design-logo-EAB6B3D5D9-seeklogo.com.png",
          alt: "ant-design",
          link: "https://www.ant.design",
        },
        {
          icon: "https://raw.githubusercontent.com/styled-components/brand/bde053200192814dcd55923b6e41884d18e51665/styled-components.svg",
          alt: "styled-components",
          link: "https://www.styled-components.com",
        },

        {
          icon: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/firebase/firebase.png",
          alt: "firebase",
          link: "https://www.firebase.google.com",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.ctn {
  background-color: #faeded;
  box-shadow: 0px 4px 10px rgba(187, 225, 250, 0.25);
  padding: 30px 150px;
  @media (max-width: 768px) {
    padding: 5px 0px;
  }
}
h4 {
  color: var(--black);
}
.headCtn {
  display: flex;
  margin: 0px 10px;
  justify-content: center;
  align-items: center;
  font-size: 22px;
  @media (max-width: 992px) {
    margin: 10px 0px;
  }
}
.lang {
  padding: 8px;
}
.langCtn {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  min-width: 30%;
  text-align: center;
}
</style>
