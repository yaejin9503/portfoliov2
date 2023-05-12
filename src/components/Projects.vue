<template lang="">
  <div>
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>
        <div class="swiper-wrap">
          <a
            href="https://highschool.jinhak.com/tendency/university-test"
            target="_blank"
          >
            <img src="../assets/img/project_img_1.png" />
          </a>
          <div class="third-contents-wrap">
            <div>
              <p class="sub-title">고등학생들을 위한 학습 성향 테스트사이트</p>
              <h3 class="title">진로 진단 검사</h3>
              <p class="sub-contents-txt mt5">
                고등학생들을 위한 학습 성향을 진단하는 사이트로 프로젝트 구성,
                구현, 배포까지 담당해서 진행했던 프로젝트 입니다. Nuxt.js로
                구현하여, SSR 방식으로 동작하게끔 개발하였고, MiddleWare로
                로그인처리 및 Vuex로의 데이터 처리 등 프로젝트의 전체적인 부분을
                개발하였습니다.
              </p>
              <div class="mt5">
                <b>사용기술</b>
                <p class="third-step sub-contents-txt">
                  Nuxt.js, Vuex, Express.js, Nest.js, TypeORM, Node.js, MSSQL,
                  Git, Docker, Kubernetes, webpack
                </p>
              </div>
              <div class="mt5">
                <b>사용도구</b>
                <p class="third-step sub-contents-txt">
                  Visual Studio Code, Prettier, ESLint, SourceTree
                </p>
              </div>
            </div>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="swiper-wrap">
          <a
            href="https://hakjong.jinhak.com/Hakjong/PassTalk/Main?TopFlag=S"
            target="_blank"
          >
            <img src="../assets/img/project_img_2.png" />
          </a>
          <div class="third-contents-wrap">
            <div>
              <p class="sub-title">고12 학생들을 위한 입시 정보 사이트</p>
              <h3 class="title">학생부 종합</h3>
              <p class="sub-contents-txt mt5">
                고등학교 1,2학년 학생들을 상대로 입시 정보를 주는 사이트로
                프로젝트 구성, 구현, 배포까지 담당해서 진행했던 프로젝트 입니다.
                CI/CD 적용, 접속 log 처리 등 프로젝트의 전체적인 부분을
                개발하였습니다.
              </p>
              <div class="mt5">
                <b>사용기술</b>
                <p class="third-step sub-contents-txt">
                  Nuxt.js, Vue.js, Vuex, Express.js, Node.js, MSSQL, Git,
                  Docker, Kubernetes
                </p>
              </div>
              <div class="mt5">
                <b>사용도구</b>
                <p class="third-step sub-contents-txt">
                  Visual Studio Code, Prettier, ESLint, SourceTree
                </p>
              </div>
            </div>
          </div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";

export default {
  name: "slider",
  data() {
    return {
      swiperOption: {
        slidesPerView: 1,
        spaceBetween: 30,
        loop: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        autoplay: {
          delay: 5000,
          disableOnInteraction: false,
        },
      },
    };
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>
