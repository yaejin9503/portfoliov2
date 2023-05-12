<template lang="">
  <div>
    <ul class="career-menu-wrap">
      <li
        :class="seletedCareerTab === 'Jinhak' ? 'selected' : ''"
        @click="seletedCareerTab = 'Jinhak'"
      >
        Jinhak
      </li>
      <li
        :class="seletedCareerTab === 'Buzz' ? 'selected' : ''"
        @click="seletedCareerTab = 'Buzz'"
      >
        Buzz&Beyond
      </li>
    </ul>
    <div class="career-container">
      <div class="title">
        <h3>
          {{ careerData[seletedCareerTab].title
          }}<span class="font-color-blue"
            >&nbsp;@{{ careerData[seletedCareerTab].company }}</span
          >
        </h3>
        <span class="date">{{ careerData[seletedCareerTab].date }}</span>
      </div>
      <div class="career-container-wrap">
        <div
          v-for="(item, index) in careerData[seletedCareerTab].contents"
          :key="index"
        >
          <h5 class="main-text">
            {{ item.title }}
          </h5>
          <div class="sub-text-wrap">
            <p v-for="(content, i) in item.subContents" :key="i">
              <span v-html="content"></span>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      seletedCareerTab: "Jinhak",
      careerData: {
        Jinhak: {
          company: "Jinhak",
          title: "웹 풀스택 개발",
          date: "2021.11~",
          contents: [
            {
              title:
                "기존에 운영되던 .NET 기반 서비스를 Nuxt.js, Express.js 기반 프로젝트로 전환 및 코드 리팩토링 진행",
              subContents: [
                "초기 프로젝트 구성, 구현, 배포, 운영까지 2개의 프로젝트 리드",
                "기존에 운영되던 서비스에서 불필요한 데이터 호출 제거 <br/>=> 사용자의 편의성 및 반응 속도 증대",
                "기존 리눅스 서버 배포 방식에서 Docker로 기반으로 변경 ( 배포 자동화 적용 ) <br/> => 배포에 드는 시간적 비용 감소",
                "초기 개발 시 CSR이였던 부분을 SSR 방식으로 변경 <br/> => 새로고침 시 깜빡거림 감소",
              ],
            },
            {
              title: " MSA 아키텍처 프로젝트를 위한 마이크로 서비스 개발",
              subContents: [
                "기존에 있던 서비스(.Net 기반) 에 독립적인 Vue.js 기반 프로젝트 개발 후 추가",
                "프로젝트 연결에 필요한 IIS 세팅 및 서버 세팅",
                ".NET WebForm 형식의 프로젝트에서 기존 인증 체계 공유를 위한 .NET MVC 프로젝트 생성 후 그 프로젝트에서 Vue.js 코드가 작동할 수 있게 개발",
              ],
            },
          ],
        },
        Buzz: {
          company: "Buzz&Beyond",
          title: "웹 풀스택 개발",
          date: "2020.06 ~ 2021.10",
          contents: [
            {
              title:
                "Youtube 데이터를 기반으로 프론트 설계 및 구현, 반응형 UI 도입 및 적용, 데이터 시각화를 위한 Chart.js 적용 ",
              subContents: [
                "Youtube 데이터를 이용한 데이터 시각화 ( Chart.js 사용 )",
                "반응형 UI 적용으로 디바이스 크기에 따른 최적화 작업",
                "RESTful API로 사내 신규 프로젝트 구현",
                "자사 멤버십 단계 추가로 인한 멤버십 로직 변경 멤버십 체계 3개 → 4개로 변경 ",
              ],
            },
          ],
        },
      },
    };
  },
};
</script>
<style lang=""></style>
