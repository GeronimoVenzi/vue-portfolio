<template>
  <section class="skills-section mt-5">
    <div class="container">
      <h2 class="text-center fw-bold">Skills</h2>
      <div class="row">
        <div class="col-md-4" v-for="column in columns" :key="column.id">
          <div class="d-flex flex-column justify-content-center align-items-center" style="height: 100%;">
            <a v-for="logo in column.logos" :key="logo.id" :href="logo.documentationLink" target="_BLANK" class="logo-container">
              <img :src="logo.src" :alt="logo.alt" class="logo" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import htmlLogo from "@/assets/html-logo.png";
import cssLogo from "@/assets/css-logo.png";
import jsLogo from "@/assets/js-logo.png";
import vueLogo from "@/assets/vue-logo.png";
import reactLogo from "@/assets/react-logo.png";
import gitLogo from "@/assets/git-logo.png";
import bootstrapLogo from "@/assets/bootstrap-logo.png";
import sassLogo from "@/assets/sass-logo.png";
import nodejsLogo from "@/assets/nodejs-logo.png";
import mysqlLogo from "@/assets/mysql-logo.png";
import dockerLogo from "@/assets/docker-logo.png";

export default {
  data() {
    return {
      columns: [
        {
          id: 1,
          logos: [
            { id: 1, src: htmlLogo, alt: "HTML", documentationLink: "https://developer.mozilla.org/docs/Web/HTML" },
            { id: 2, src: cssLogo, alt: "CSS", documentationLink: "https://developer.mozilla.org/docs/Web/CSS" },
            { id: 3, src: jsLogo, alt: "JavaScript", documentationLink: "https://developer.mozilla.org/docs/Web/JavaScript" }
          ]
        },
        {
          id: 2,
          logos: [
            { id: 4, src: vueLogo, alt: "Vue.js", documentationLink: "https://vuejs.org" },
            { id: 5, src: reactLogo, alt: "React", documentationLink: "https://reactjs.org" },
            { id: 6, src: gitLogo, alt: "Git", documentationLink: "https://git-scm.com/doc" },
            { id: 7, src: bootstrapLogo, alt: "Bootstrap", documentationLink: "https://getbootstrap.com/docs" }
          ]
        },
        {
          id: 3,
          logos: [
            { id: 8, src: sassLogo, alt: "Sass", documentationLink: "https://sass-lang.com/documentation" },
            { id: 9, src: nodejsLogo, alt: "Node.js", documentationLink: "https://nodejs.org/docs/latest/api" },
            { id: 10, src: dockerLogo, alt: "Docker", documentationLink: "https://docs.docker.com" },
            { id: 11, src: mysqlLogo, alt: "MySQL", documentationLink: "https://dev.mysql.com/doc" }
          ]
        }
      ]
    };
  }
};
</script>

<style scoped>
.logo-container {
  text-align: center;
  margin-bottom: 20px;
  transition: transform 0.5s linear;
}

.logo-container:hover {
  transform: scale(1.3);
}
.logo {
  width: 100px;
  height: auto;
}
</style>




<!-- 
<template>
  <section class="skills-section">
    <div class="container">
      <h2 class="text-center">Skills</h2>
      <div class="row mt-4">
        <div class="col-md-4" v-for="column in columns" :key="column.id">
          <div class="d-flex flex-column justify-content-center align-items-center" style="height: 100%;">
            <div v-for="logo in column.logos" :key="logo.id" class="logo-container">
              <img :src="logo.src" :alt="logo.alt" class="logo" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import htmlLogo from "@/assets/html-logo.png";
import cssLogo from "@/assets/css-logo.png";
import jsLogo from "@/assets/js-logo.png";
import vueLogo from "@/assets/vue-logo.png";
import reactLogo from "@/assets/react-logo.png";
import gitLogo from "@/assets/git-logo.png";
import bootstrapLogo from "@/assets/bootstrap-logo.png";
import sassLogo from "@/assets/sass-logo.png";
import nodejsLogo from "@/assets/nodejs-logo.png";
import mysqlLogo from "@/assets/mysql-logo.png";
import dockerLogo from "@/assets/docker-logo.png";

export default {
  data() {
    return {
      columns: [
        {
          id: 1,
          logos: [
            { id: 1, src: htmlLogo, alt: "HTML" },
            { id: 2, src: cssLogo, alt: "CSS" },
            { id: 3, src: jsLogo, alt: "JavaScript" }
          ]
        },
        {
          id: 2,
          logos: [
            { id: 4, src: vueLogo, alt: "Vue.js" },
            { id: 5, src: reactLogo, alt: "React" },
            { id: 6, src: gitLogo, alt: "Git" },
            { id: 7, src: bootstrapLogo, alt: "Bootstrap"  },
          ]
        },
        {
          id: 3,
          logos: [
            { id: 8, src: sassLogo, alt: "Sass" },
            { id: 9, src: nodejsLogo, alt: "Node.js" },
            { id: 10, src: dockerLogo, alt: "Docker" },
            { id: 11, src: mysqlLogo, alt: "MySQL" }
          ]
        }
      ]
    };
  }
};
</script>

<style scoped>
.logo-container {
  text-align: center;
  margin-bottom: 20px;
}

.logo {
  width: 100px;
  height: auto;
}
</style> -->
