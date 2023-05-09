<template lang="">
  <div class="container">
    <section class="first-step-wrap">
      <div>
        <p>안녕하세요🙌</p>
        <p>
          Front-end Developer <br />
          <b>김예진</b> 입니다.
        </p>
        <p>
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
      <div class="second-container">
        <h3>💻Where I’ve <span class="font-color-blue">Worked</span></h3>
        <div>
          <ul class="career-menu-wrap">
            <li class="selected">Jinhak</li>
            <li>Buzz&Beyond</li>
          </ul>
          <div class="career-container">
            <div>
              <h3>웹 풀스택 개발 <span>@Jinhak</span></h3>
              <span>2021.11~</span>
            </div>
            <div class="career-container-wrap">
              <div>
                <h5 class="text">
                  기존에 운영되던 .NET 기반 서비스를 Nuxt.js, Express.js 기반
                  프로젝트로 전환 및 코드 리팩토링 진행
                </h5>
                <p></p>
              </div>
              <div>
                <h5></h5>
                <p></p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section></section>
    <section></section>
    <div class="tab-wrap">
      <ul>
        <li class="selected">About</li>
        <li>Career</li>
        <li>Projects</li>
        <li>Skills</li>
      </ul>
      <div class="left-line"></div>
      <div class="circle-wrap">
        <div class="circle"></div>
      </div>
    </div>
  </div>
</template>
<script>
// import Introduce from "./Introduce.vue";

export default {
  name: "App",
  components: {
    // Introduce,
  },
};
</script>
