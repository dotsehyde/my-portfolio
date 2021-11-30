<template>
  <div id="profile">
    <p class="heading">" Education "</p>
    <EduCard
      v-for="edu in education"
      :key="edu.cert"
      :title="edu.title"
      :date="edu.date"
      :cert="edu.cert"
      :loc="edu.loc"
    />

    <p class="workTitle">{{ workText }}</p>
    <div class="exp">
      <EduCard
        v-for="ex in experience"
        :key="ex.title"
        :title="ex.title"
        :date="ex.date"
        :cert="ex.cert"
        :loc="ex.loc"
      />
    </div>
  </div>
</template>
<script>
import EduCard from "../components/EduCard.vue";
export default {
  name: "profile",
  components: {
    EduCard,
  },
  data() {
    return {
      workText: "{ Work Experience }",
      education: [
        {
          title: "True Love School",
          date: "Completed 2015",
          cert: "B.E.C.E",
          loc: "East Legon, Accra",
        },
        {
          title: "Mawuli Senior High School",
          date: "2015 - 2018",
          cert: "W.A.C.E",
          loc: "Ho, Volta",
        },
        {
          title: "Ghana Technology University College",
          date: "2018 - 2020",
          cert: "Diploma in IT",
          loc: "Tesano, Accra",
        },
      ],
      experience: [
        {
          title: "Agrihouse Foundation",
          date: "Jun 2020 - Dec 2021",
          cert: "Contract",
          loc: "Web Developer",
        },
        {
          title: "Sacrefilms Multimedia",
          date: "Oct 2020 - May 2021",
          cert: "Contract",
          loc: "Video/Photo Editor",
        },
        {
          title: "Branfluenzas",
          date: "Jun 2021 - Sep 2021",
          cert: "Internship",
          loc: "Mobile Developer",
        },
        {
          title: "Wookin, Inc.",
          date: "Sep 2021 - Nov 2021",
          cert: "Contract",
          loc: "Mobile Developer",
        },
        {
          title: "Syka Bank",
          date: "Sep 2021 - Present",
          cert: "Part Time (Coding Group)",
          loc: "Mobile Developer",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
#profile {
  padding: 25px 0;
}
.exp {
  display: grid;
  grid-template-columns: auto auto;
  place-items: left;

  /* @media (max-width: 992px) {
    grid-template-columns: auto;
    place-items: center;
  } */
  @media (max-width: 992px) {
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
.workTitle {
  background: #effaed;
  color: var(--black);
  font-weight: bold;
  font-size: 40px;
  text-align: center;
  margin-top: 15px;
  padding: 20px 150px;
  @media (max-width: 768px) {
    padding: 10px 0;
    font-size: 30px;
  }
}
.heading {
  color: #21243d;
  font-weight: bold;
  font-size: 40px;
  /* margin-top: 30px; */
  padding: 0 150px;
  @media (max-width: 768px) {
    text-align: center;
    padding: 0;
    font-size: 32px;
  }
}
</style>
