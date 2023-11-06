 <template lang="">
  <div class="container">
   <div class="menu">
     <ul>
       <!--:class="top >=aboutTop && top < careerTop ? 'selected' : '' "-->
       <li @click="clickMenu('first-step-wrap')">
        <a href="javascript:void(0)">
          <span>About</span>
        </a>
       </li>
       <li @click="clickMenu('second-step-wrap')">
        <a href="javascript:void(0)">
          <span>Career</span>
        </a>
       </li>
       <li @click="clickMenu('third-step-wrap')">
        <a href="javascript:void(0)">
          <span>Projects</span>
        </a>
       </li>
       <li  @click="clickMenu('fourth-step-wrap')">
        <a href="javascript:void(0)">
          <span>Skills</span>
        </a>
       </li>
     </ul>
   </div>
    <section> 
      <div class="name-container">
        <div id="title-1" class="title top">WEB<br/>DEVELPLER</div>
        <div id="title-2" class="title bottom">KIMYEJIN</div>
      </div>
    </section>
    <section class="first-step-wrap">
      <div>
        <p style="animation-delay: 0s;">안녕하세요🙌</p>
        <p style="animation-delay: 1s;">
          <span>Web Developer</span><br />
        </p>
        <p>
          <span class="font-color-blue name-t"></span>
          <span>입니다.</span>
        </p>
        <p class="mt5" style="animation-delay: 2s;">
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
          <a class= "" href="https://ember-fontina-aa1.notion.site/3-e17710cf8a89419a8dbb0a8b49d28e84" target="_blank">
            <button>Resume</button>
          </a>
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
          <div>
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
      </div>
    </section>
    <div class="tab-wrap" style="display:none">
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
      aboutTop : 0, 
      careerTop : 0, 
      projectsTop : 0, 
      skillsTop : 0 
    };
  },
  mounted() {
    // document.addEventListener("scroll", this.scrollEvents); 
    // this.show(); 

    window.onload = function(){
      const elm = document.querySelectorAll('section');
      const elmCount = elm.length;
      elm.forEach(function(item, index){
        item.addEventListener('mousewheel', function(event){
          event.preventDefault();
          let delta = 0;

          if (!event) event = window.event;
          if (event.wheelDelta) {
              delta = event.wheelDelta / 120;
              if (window.opera) delta = -delta;
          } 
          else if (event.detail)
              delta = -event.detail / 3;

          let moveTop = window.scrollY;
          let elmSelector = elm[index];

          // wheel down : move to next section
          if (delta < 0){
            if (elmSelector !== elmCount-1){
              try{
                moveTop = window.pageYOffset + elmSelector.nextElementSibling.getBoundingClientRect().top;
              // eslint-disable-next-line no-empty
              }catch(e){}
            }
          }
          // wheel up : move to previous section
          else{
            if (elmSelector !== 0){
              try{
                moveTop = window.pageYOffset + elmSelector.previousElementSibling.getBoundingClientRect().top;
              // eslint-disable-next-line no-empty
              }catch(e){}
            }
          }

          // eslint-disable-next-line no-unused-vars
          const body = document.querySelector('html');
          window.scrollTo({top:moveTop, left:0, behavior:'smooth'});
        });
      });
    }
    
    this.aboutTop = document.querySelector('.first-step-wrap').offsetTop;
    this.careerTop =  document.querySelector('.second-step-wrap').offsetTop; 
    this.projectsTop = document.querySelector('.third-step-wrap').offsetTop; 
    this.skillsTop = document.querySelector('.fourth-step-wrap').offsetTop; 
  
    const $text = document.querySelector('.name-t'); 
    const letters = ['김예진']; 
    const speed = 150; // 속도 
    let i = 0; // 현재 지정된 글자  


    // 타이핑 효과
    const typing = async () => {  
      const letter = letters[i].split("");
  
      while (letter.length) {
        await wait(speed);
        $text.innerHTML += letter.shift(); 
      }
  
      // 잠시 대기
      await wait(800);
  
      // 지우는 효과
      remove();
    }

  // 글자 지우는 효과
    const remove = async () => {
      const letter = letters[i].split("");
    
      while (letter.length) {
        await wait(speed);
        
        letter.pop();
        $text.innerHTML = letter.join(""); 
      }
      
      // 다음 순서의 글자로 지정, 타이핑 함수 다시 실행
      i = !letters[i+1] ? 0 : i + 1;
      typing();
    }

    // 딜레이 기능 ( 마이크로초 )
    function wait(ms) {
      return new Promise(res => setTimeout(res, ms))
    }

    // 초기 실행
    setTimeout(typing, 1500);
  
  },
  unmounted() {
    document.removeEventListener("scroll", this.scrollEvents);
  },
  methods: {
    clickMenu(className) {
      const areaTop = document.querySelector('.' + className).offsetTop; 

      window.scroll({ top : areaTop, behavior: "smooth" }); 
      this.top = areaTop; 
    },

    // scrollEvents() {
    //   this.top = document.scrollingElement.scrollTop
    //   if(this.top > 100) { 
    //     this.disappear(); 
    //   }else{ 
    //     this.show();
    //   }
    // },
  },
};
</script>
