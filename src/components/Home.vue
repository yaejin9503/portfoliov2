<template lang="">
  <div class="container">
    <section class="first-step-wrap">
      <div>
        <p>안녕하세요🙌</p>
        <p>
          Front-end Developer<br />
          <b class="font-color-blue">김예진</b> 입니다.
        </p>
        <p class="mt5">
          3년차 개발자로 스타트업과 자사 플랫폼을 운영하는 회사에서 웹서비스를
          개발/배포/운영 하였습니다.<br />
          2개의 프로젝트를 리드한 경험이 있어 개발의 한 사이클을 이해하고 개발할
          수 있습니다.
          <br /><br />
          최근에는 불필요한 렌더링을 최소화 하는 작업에 집중하고 있고, 기존에
          구현했던 코드를 리팩토링 하며, <br />
          보완해야 할 부분을 찾는 것을 좋아합니다.
        </p>
        <div>
          <button>Resume</button>
        </div>
      </div>
    </section>
    <section class="second-step-wrap">
      <div class="second-step contents-container">
        <h3 class="section-title">
          💻Where I’ve <span class="font-color-blue">Worked</span>
        </h3>
        <Career />
      </div>
    </section>
    <section class="third-step-wrap">
      <div class="third-step contents-container">
        <h3 class="section-title font-color-blue">📢 Projects</h3>
        <Projects />
      </div>
    </section>
    <section class="fourth-step-wrap">
      <div class="fourth-step contents-container">
        <h3 class="section-title font-color-blue">✨Skills</h3>
        <div class="fourth-step contents-wrap">
          <IconImg
            :src="'https://cdn-icons-png.flaticon.com/512/5968/5968292.png'"
            :title="'JavaScript'"
          />
          <IconImg
            :src="'https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1184px-Vue.js_Logo_2.svg.png'"
            :title="'Vue'"
          />
          <IconImg
            :src="'https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Nuxt_logo.svg/2560px-Nuxt_logo.svg.png'"
            :title="'Nuxt'"
          />
          <IconImg
            :src="'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png'"
            :title="'NodeJS'"
          />
          <IconImg
            :src="'https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/2300px-React-icon.svg.png'"
            :title="'React'"
          />
          <IconImg
            :src="'https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Typescript_logo_2020.svg/2048px-Typescript_logo_2020.svg.png'"
            :title="'TypeScript'"
          />
        </div>
        <div class="fourth-step contents-wrap mt10">
          <IconImg
            :src="'https://upload.wikimedia.org/wikipedia/commons/a/a8/NestJS.svg'"
            :title="'NestJS'"
          />
          <IconImg
            :src="'https://www.docker.com/wp-content/uploads/2022/03/vertical-logo-monochromatic.png'"
            :title="'Docker'"
          />
          <IconImg
            :src="'https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/CSS3_logo.svg/800px-CSS3_logo.svg.png'"
            :title="'CSS'"
          />
          <IconImg
            :src="'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png'"
            :title="'Git'"
          />
          <IconImg
            :src="'https://raw.githubusercontent.com/webpack/media/master/logo/icon-square-big.png'"
            :title="'Webpack'"
          />
        </div>
      </div>
    </section>
    <div class="tab-wrap">
      <ul>
        <li
          :class="selectedMenu === 1 ? 'selected' : ''"
          @click="clickMenu('first-step-wrap', 1)"
        >
          About
        </li>
        <li
          :class="selectedMenu === 2 ? 'selected' : ''"
          @click="clickMenu('second-step-wrap', 2)"
        >
          Career
        </li>
        <li
          :class="selectedMenu === 3 ? 'selected' : ''"
          @click="clickMenu('third-step-wrap', 3)"
        >
          Projects
        </li>
        <li
          :class="selectedMenu === 4 ? 'selected' : ''"
          @click="clickMenu('fourth-step-wrap', 4)"
        >
          Skills
        </li>
      </ul>
      <div class="left-line"></div>
      <div class="circle-wrap">
        <div class="circle" :style="`top:${top}%`"></div>
      </div>
    </div>
  </div>
</template>
<script>
// import Introduce from "./Introduce.vue";
import Projects from "./Projects.vue";
import Career from "./Career.vue";
import IconImg from "./common/IconImg.vue";

export default {
  name: "App",
  components: {
    Projects,
    Career,
    IconImg,
  },
  data() {
    return {
      selectedMenu: 1,
      top: 10,
    };
  },
  methods: {
    clickMenu(className, menuNum) {
      document
        .querySelector("." + className)
        .scrollIntoView({ behavior: "smooth" });
      this.selectedMenu = menuNum;
      this.top =
        menuNum === 1 ? 10 : menuNum === 2 ? 35 : menuNum === 3 ? 60 : 90;
    },
  },
};
</script>
