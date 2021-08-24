<template>
  <q-layout view="lHh lpr lFf">
    <div v-bind:class="{'main': $q.platform.is.desktop, 'mobile_main': $q.platform.is.ipad || $q.platform.is.mobile}"
         class="full-height" style="background-color:rgba(0, 0, 0, 0.7);">

      <q-header class="q-py-sm" style="background-color:rgba(0, 0, 0, 0.7);">
        <q-toolbar class="text-h4">
          <q-space></q-space>
          <q-tabs v-model="selected_tab" shrink>
            <q-tab name="about_me" :style="[selected_tab == 'about_me' ? {backgroundColor: 'green'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_about_me')" style="width:120px;min-height:auto !important;color: white"
                   label="About Me"/>
            <q-tab name="portfolio" :style="[selected_tab == 'portfolio' ? {backgroundColor: 'green'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_projects')" style="width:120px;min-height:auto !important;color: white"
                   label="portfolio"/>
            <q-tab name="certificate" :style="[selected_tab == 'certificate' ? {backgroundColor: 'green'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_publications')" style="width:120px;min-height:auto !important;color: white"
                   label="certificate"/>
            <!-- <q-tab name="photo" :style="[selected_tab == 'photo' ? {backgroundColor: 'green'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_photo')" style="width:120px;min-height:auto !important;color: white"
                   label="Photo"/> -->
            <q-tab name="contact" :style="[selected_tab == 'contact' ? {backgroundColor: 'green'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_contact_me')"
                   style="width:120px;min-height:auto !important;color: white" label="Contact Me"/>
          </q-tabs>
        </q-toolbar>
      </q-header>
      <section>
        <div class="full-height full-width flex flex-center text-center"
           style="background-color: rgba(0, 0, 0, 0.68) !important;z-index:0;height: 100vh !important;">
        <div class="">
          <div class="text-h6 text-grey-5">WELCOME TO MY PAGE</div>
          <div class="text-h2 text-white q-py-sm q-my-md"
               style="border-top:3px solid #1595de;border-bottom: 3px solid #2faa64;">I'M a JUNIOR DEVELOPER.
          </div>
          <div class="text-h6" style="color: #f4b825;">
            S/W DEVELOPER | FULL STACK JUNIOR ENGINEER | JOB SEEKER
          </div>
          <div style="color: #1495de !important;" class="text-h4 q-mt-md text-grey-2 my-font">
            DUYONG BAEK
          </div>
        </div>
      </div>
      </section>
    </div>

    <div style="background-color:#33495e" id="id_about_me">
      <div class="row">
        <div class="col-md-4 col-lg-4 col-xs-12 col-sm-12">
          <div style="background-color:#ea4946" class="q-pa-md text-center text-white text-weight-bolder text-h4">
            ABOUT ME
          </div>
          <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
            <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
              <q-img style="height:600px"
                     class="col-5"
                     src="/statics/images/IMG_8952.jpg"
              />
            </div>
          </div>
        </div>
        <div class="col-md-8 col-lg-8 col-xs-12 col-sm-12 q-px-md q-pt-sm">
          <div class="text-h4 text-center text-white q-py-xs q-my-xs"
               style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">HELLO
          </div>
          <h5 class="q-my-none text-caption" style="color: #20ffff;">
            2021.03 ~ 현재 : 한국폴리텍대학 서울강서캠퍼스 &lt;재학중&gt;<br>
            - 스마트 금융과<br>
            - Python(machine learning, Data Preprocessing, Data analysis, ETL, crawling)<br>
            - Java(Spring, Spring Boot, Egovframework)<br>
            - Javascript(vue.js, Quasar)<br>
            - Linux(CentOS, Ubuntu)<br>
            - Database(Oracle, Mysql, MongoDB)
            <br>
            <br>
            2015.03 ~ 2021.02 : 한신대학교 &lt;졸업&gt;<br>
            - 국제경제학과
            <br>
            <br>
            2016.03 ~ 2021.02 : 한신대학교 사회봉사단 HAHA<br>
            - 2020.01 ~ 2021.02 단장(봉사단 총괄업무 수행)<br>           
            - 2019.01 ~ 2019.12 운영부장(봉사단 행사, 회계업무 수행)
            <br>
            <br>
            2020.09 ~ 2020.10 : 청년친화강소기업 서포터즈<br>
            - 고용노동부 선정 청년친화강소기업 취재
            <br>
            <br>
            2020.01.03 ~ 2021.02.28 : 국민은행<br>
            - 인턴(영업점 내 비대면 채널업무 수행)
            <br>
            <br>
            2018.10 ~ 2019.03 : 한신대학교 해외봉사단 네팔드림<br>
            - 네팔 바굴룽지역 교육 및 문화 활동 진행<br>
            - 회계(봉사단 회계업무 수행)<br>
            - 키퍼(봉사단 규칙 지킴이)
            <br>
            <br>
            2016.08 ~ 2018.05 : 병역 필<br>
            <br>
            <br>
          </h5>
        </div>
      </div>
    </div>
    <div style="background-color:#2b5873" id="id_projects">
      <div class="row q-px-xl">
        <div class="text-h4 text-center text-white q-py-sm q-my-md full-width"
             style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">My Portfolio
        </div>
        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section>
              <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://github.com/DUYONGBEAK/FRS_SpringFramework" target="_blank">FORK ME ON GITHUB!</a>
              </q-ribbon>
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-overline text-pink">2021 Problem Prototype Practice</div>
                    <div class="text-h5 q-mt-sm q-mb-xs">
                      <a class="project_link" style="text-decoration: none;color: #eb4f71;"
                         href="http://52.79.106.72/" target="_blank">Financial Products Recommendation Service</a>
                    </div>
                    <div class="text-caption text-grey-9">
                      Financial service using web crawling and machine learning
                      <ul>
                        <li>Spring Framework</li>
                        <li>MariaDB</li>
                        <li>JSP and JSTL</li>
                        <li>bootstrap</li>
                        <li>Machine Learning with Python</li>
                        <li>Session Processing</li>
                        <li>Member Management</li>
                        <li>Amazon Web Services</li>
                      </ul>
                    </div>
                  </q-card-section>
                </div>
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/frs.png"
                    />
                  </q-card-section>
                </div>
              </div>
            </q-card-section>

            <q-separator/>

            <q-card-actions class="block">
              <a style="font-size: 25px;" class="q-py-sm q-pl-sm" href="http://52.79.106.72/"
                 target="_blank" title="SlideShare"><i class="far fa-arrow-alt-circle-left" style="color: #eb5daa">Push</i></a>
              <div class="float-right q-py-sm">
                <iframe class="float-right"
                        src="https://ghbtns.com/github-btn.html?user=DUYONGBEAK&repo=FRS_SpringFramework&type=fork&count=true&size=large"
                        frameborder="0" scrolling="0" width="136" height="30" title="GitHub"></iframe>
              </div>
            </q-card-actions>
          </q-card>
        </div>

        <!-- <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section>
              <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://www.youtube.com/channel/UCEiSIPhofgNfzacBdMpkARg" target="_blank">SUBSCRIBE ME</a>
              </q-ribbon>
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-overline text-pink">IT Lecture</div>
                    <div class="text-h5 q-mt-sm q-mb-xs">
                      <a class="project_link" style="text-decoration: none;color: #eb4f71;"
                         href="https://www.youtube.com/channel/UCEiSIPhofgNfzacBdMpkARg" target="_blank">Online Tutorial Clip</a>
                    </div>
                    <div class="text-caption text-grey-9">
                      Youtube Channel - IT Lecture for Students
                      
                      <ul>
                        <li>Algorithm</li>
                        <li>HyperLedger Fabric 2.0</li>
                        <li>iPhone App Develomnet w/ Firebase</li>
                        <li>Docker and Kubernetes</li>
                        <li>Kafka, ShardingSphere, Redis...</li>
                        <li>Stock Forecasting</li>
                      </ul>
                    </div>
                  </q-card-section>
                </div>
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/youtube.png"
                    />
                  </q-card-section>
                </div>
              </div>
            </q-card-section>

            <q-separator/>

            <q-card-actions class="block">
              <a style="font-size: 25px;" class="q-py-sm q-pl-sm" href="https://www.youtube.com/channel/UCEiSIPhofgNfzacBdMpkARg"
                 target="_blank" title="Donate"><i class="fab fa-youtube" style="color: #eb5daa"></i></a>
              
            </q-card-actions>
          </q-card>
        </div> -->

        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section>
              <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://github.com/DUYONGBEAK/MyStockModel" target="_blank">FORK ME ON GITHUB!</a>
              </q-ribbon>
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-overline text-pink">Smart Finance</div>
                    <div class="text-h5 q-mt-sm q-mb-xs">
                      <a class="project_link" style="text-decoration: none;color: #eb4f71;"
                         href="https://github.com/wonyongHwang/kopoStockModel" target="_blank">CCI Stock Model</a>
                    </div>
                    <div class="text-caption text-grey-9">
                      이 함수는 일정기간 주식의 CCI지표를 볼수있도록 값을 구해줍니다.<br>
                      단, 종가는 주식시장에서 보여지는 있는 그대로의 종가를 사용했기 때문에<br> 
                      수정종가를 사용하는 실제 CCI에 비해 정확도가 떨어질 수 있습니다.
                      <ul>
                        <li>matplotlib, pandas, numpy, scipy</li>
                        <li>finance-datareader</li>
                        <li>beautifulsoup4</li>
                        <li>mplfinance</li>
                        <li>chart-studio</li>
                        <li>plotly</li>
                        <li>REST API</li>
                        <li>Threading</li>
                        <li>Socket Server</li>

                      </ul>
                    </div>
                  </q-card-section>
                </div>
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/CCI.png"
                    />
                  </q-card-section>
                </div>
              </div>
            </q-card-section>

            <q-separator/>

            <q-card-actions class="block">
              <div class="float-right q-py-sm">
                <iframe class="float-right"
                        src="https://ghbtns.com/github-btn.html?user=DUYONGBEAK&repo=MyStockModel&type=fork&count=true&size=large"
                        frameborder="0" scrolling="0" width="136" height="30" title="GitHub"></iframe>
              </div>
            </q-card-actions>
          </q-card>
        </div>
      </div>
    </div>

    <div style="background-color:#14104e" id="id_publications">
      <div class="row row q-px-xl">
        <div class="text-h4 text-center text-white q-py-sm q-my-md full-width"
             style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">Certificate & License
        </div>
        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section class="q-py-xs">
              <div class="text-overline text-pink">Certificate</div>
                
                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">SQLD(SQL 개발자, Structured Query Language Developer)</div>
                </div>
                <div class="text-caption text-grey-9">
                  Jun, 2021 KOREA Data Agency<br>
                  <br>
                  SQL (SQLD*, SQL Developer) We are operating software development data to cope with database and data, <br>
                  and are currently supporting SQL developers.<br>  
                <br>
                </div>

                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">CCA(신용분석사, Certified Credit Analyst)</div>
                </div>
                <div class="text-caption text-grey-9">
                  Nov, 2020 KOREA BANKING INSTITUTE<br>
                  <br>
                  A financial expert in charge of corporate credit evaluation, such as determining the overall credit situation and credit rating,<br> 
                  through the analysis of accounting and non-accounting data on the company in the credit-related department of a financial institution.<br>  
                <br>
                </div>

                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">AFPK(재무설계사, ASSOCIATE FINANCIAL PLANNER KOREA)</div>
                </div>
                <div class="text-caption text-grey-9">
                  Jun, 2020 FPSB Korea<br>
                  <br>
                  AFPK certifiers are professionals with expertise in providing services related<br>  
                  to financial planning and ethics that put the interests of customers first.<br>
                <br>
                </div>

            </q-card-section>
          </q-card>
        </div>

        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section class="q-py-xs">
              
                <div class="text-overline text-pink">License</div>
                
                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">정보처리기사(Engineer Information Processing)</div>
                </div>
                <div class="text-caption text-grey-9">
                  Nov, 2021 Human Resources Development Service of Korea<br>
                  <br>
                  As a software development-related certification, it is an exam that verifies the ability to perform tasks such as <br>
                  planning, analysis, design, implementation, testing, operation, and maintenance <br>
                  as a job performing project tasks throughout the life cycle of information systems.<br>  
                <br>
                </div>

                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">CIM(투자자산운용사, Certified Investment Manager)</div>
                </div>
                <div class="text-caption text-grey-9">
                  Jun, 2020 Korea Financial Investment Association<br>
                  <br>      
                  A person who manages collective investment property, trust property, or discretionary investment property<br> 
                <br>
                </div>

            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>

   <!--  <section id="id_photo">
      <div style="background-color:#206b73;z-index:0;" class="content">
        <div class="row row q-px-xl">
          <div class="text-h4 text-center text-white q-py-sm q-my-md full-width"
               style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">Photo
          </div>
          <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl">
            <div class="q-pa-md">
              <div class="q-col-gutter-md row">
                <div class="col-md-6 col-md-6 col-xs-12 col-sm-12 text-center flex flex-center">
                  <q-img
                    src="statics/images/pic1.png"
                    v-bind:class="{'sketch_desktop': $q.platform.is.desktop, 'sketch_mobile': $q.platform.is.ipad || $q.platform.is.mobile}"
                  >
                  </q-img>
                </div>
              
                <div class="col-md-6 col-md-6 col-xs-12 col-sm-12 text-center flex flex-center">
                  <q-img src="statics/images/pic2.png"
                         v-bind:class="{'sketch_desktop': $q.platform.is.desktop, 'sketch_mobile': $q.platform.is.ipad || $q.platform.is.mobile}">
                  </q-img>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>-->
      <!-- <canvas id="canvas2" style="height: 100%;width:100%;"></canvas> -->
    <!--</section> -->
    
    <div id="contact_us">
      <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
        <form
          action="https://formspree.io/f/xleaovly"
          method="POST"
        >
          <div class="row text-center flex flex-center q-py-lg">
            <div class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none">
              <q-input required v-model="name" name="name" bg-color="white" outlined label="Your Name *">
                <template v-slot:append>
                  <q-icon name="list" style="color:green"/>
                </template>
              </q-input>
              <q-input type="email" required v-model="email" name="_replyto" bg-color="white" outlined label="Your Email *">
                <template v-slot:append>
                  <q-icon name="email" style="color:green"/>
                </template>
              </q-input>
            </div>
            <div class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none">
              <q-input required v-model="message" name="message" class="" type="textarea" bg-color="white" outlined
                       label="Your Message *">
                <template v-slot:append>
                  <q-icon name="comment" style="color:green"/>
                </template>
              </q-input>
            </div>
          </div>
          <div class="row flex flex-center text-center q-pb-xl q-mt-md">
            <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12">
              <q-btn type="submit" size="lg" style="background:green;color: white" label="Send Message"/>
            </div>
          </div>
        </form>
      </div>
    </div>
    <q-toolbar class="flex flex-center text-white" style="background-color: #1c1b21;border-top: 2px solid green"
               id="id_contact_me">
      <div class="q-pa-sm q-gutter-sm">
        <!-- <q-btn target="_blank" style="border: 2px solid green" round type="a" href="https://twitter.com/dreamonpanda"
               glossy
               icon="fab fa-twitter"/> -->
        <q-btn target="_blank" style="border: 2px solid green" round type="a"
               href="https://github.com/DUYONGBEAK?tab=repositories"
               glossy
               icon="fab fa-github"/>
        <q-btn style="border: 2px solid green" round type="a" href="mailto:dybaek411g@gmail.com"
               glossy
               icon="email"/>
        <q-btn target="_blank" style="border: 2px solid green;" round type="a"
               href="https://www.instagram.com/_pe_to/"
               glossy
               icon="fab fa-instagram"/>
        <!-- <q-btn target="_blank" style="border: 2px solid green;" round type="a"
               href="https://www.facebook.com/wonyong.hwang"
               glossy
               icon="fab fa-facebook"/> -->
        <!-- <q-btn target="_blank" style="border: 2px solid green;" round type="a"
               href="https://www.linkedin.com/in/justino/"
               glossy
               icon="fab fa-linkedin"/> -->
      </div>
    </q-toolbar>
  </q-layout>
</template>

<script>

    import {scroll} from 'quasar'

    const {getScrollTarget, setScrollPosition} = scroll
    export default {
        name: 'PageIndex',
        data() {
            return {
                name: "",
                email: "",
                message: "",
                selected_tab: 'about_me',
            }
        },
        methods: {
            scrollToElement(id) {
                let el = document.getElementById(id)
                const target = getScrollTarget(el)
                const offset = el.offsetTop - 65
                const duration = 800
                setScrollPosition(target, offset, duration)
            }
        },
        mounted: function () {
            // let canvas2Settings = {
            //     "target": "canvas2",
            //     "max": "120",
            //     "animate": true,
            //     "props": ["circle", "square", "triangle", "line"],
            //     "colors": [[165, 104, 246], [230, 61, 135], [0, 199, 228], [253, 214, 126]],
            //     "clock": "20"
            // };
            // let canvas2 = new ConfettiGenerator(canvas2Settings);
            // canvas2.render();
        }
    }
</script>

<style>
  .main {

    background: url(/statics/images/IMG_3444.jpg) no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    height: 100vh !important;
  }

  .mobile_main {
    background: url(/statics/images/IMG_3444.jpg) no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    height: 100vh !important;
  }

  .my-card {
    width: 100%;
    max-width: 800px;
    border: none;
    border-radius: 0px;
  }

  .sponsor-card {
    width: 100%;
    max-width: 240px;
    border: none;
    border-radius: 6px;
  }

  .project_link:hover {
    text-decoration: underline !important;
  }

  .sketch_desktop {
    width: 100%;
    height: 100%;
    display:block; 
    margin:auto;
    border: 5px solid #30313b;
  }

  .sketch_mobile {
    width: 100%;
    height: 100% !important;
    border: 20px solid #30313b;
  }

  #contact_us {
    background: url(/statics/images/20190712_203422.jpg);
    background-size: cover;
    background-position: 50%;
    background-attachment: fixed;
    background-repeat: no-repeat;
  }

  .custom_tab {
    width: 130px;
  }

  body {
    overflow-x: hidden;
  }

  section {
    position: relative;
  }

  section > * {
    z-index: 9;
    position: relative;
    top: 0;
  }

  section > canvas {
    z-index: 1;
    position: absolute;
    left: 0;
  }
</style>
