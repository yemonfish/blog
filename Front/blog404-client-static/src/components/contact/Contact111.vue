<template>
  <div class="container">
    <el-container>
      <el-header height="191px">
        <div class="info">
          <div class="margin-top">
          </div>
          <el-row class="demo-avatar demo-basic">
            <el-col :span="12">
              <div class="demo-basic&#45;&#45;circle">
                <div class="block"><el-avatar shape="square" :size="100" :src="squareUrl"></el-avatar></div>
                <div class="block" v-for="size in sizeList" :key="size">
                  <el-avatar shape="square" :size="size" :src="squareUrl"></el-avatar>
                </div>
              </div>
            </el-col>
          </el-row>
          <div class="nickname">
            鱼
          </div>
          <div class="introduce">
            404 Not Found
          </div>
        </div>
      </el-header>
      <div class="container-content">
        <div class="menu">
          <router-view></router-view>
          <el-menu
            :default-active="$route.path"
            class="el-menu-demo"
            router
            mode="horizontal"
            @select="handleSelect"
            background-color="#73aec4"
            text-color="#f9f177"
            active-text-color="white">
            <el-menu-item index="/Home">HOME</el-menu-item>
            <el-submenu index="2">
              <template slot="title">PHOTOGRAPH</template>
              <el-menu-item index="/Favorite">FAVORITE</el-menu-item>
              <el-menu-item index="/Album">ALBUM</el-menu-item>
              <el-menu-item index="/Timeline">TIMELINE</el-menu-item>
              <el-menu-item index="/Photographer">PHOTOGRAPHER</el-menu-item>
            </el-submenu>
            <el-submenu index="3">
              <template slot="title">MUSIC</template>
              <el-menu-item index="/ARTIST">ARTIST</el-menu-item>
              <el-menu-item index="/PLAYLIST">PLAYLIST</el-menu-item>
            </el-submenu>
            <el-submenu index="4">
              <template slot="title">MOVIE</template>
              <el-menu-item index="/DIRECTOR">DIRECTOR</el-menu-item>
              <el-menu-item index="/LIST">LIST</el-menu-item>
            </el-submenu>
            <el-submenu index="5">
              <template slot="title">CODE</template>
              <el-menu-item index="/Java">Java</el-menu-item>
              <el-menu-item index="/Go">Go</el-menu-item>
              <el-menu-item index="/Front-End">Front-End</el-menu-item>
              <el-menu-item index="/ALGORITHM">ALGORITHM</el-menu-item>
            </el-submenu>
            <el-submenu index="6">
              <template slot="title">READING</template>
              <el-menu-item index="/NOTE">NOTE</el-menu-item>
              <el-menu-item index="/AUTHOR">AUTHOR</el-menu-item>
            </el-submenu>
            <el-submenu index="7">
              <template slot="title">DAILY</template>
              <el-menu-item index="/JOURNAL">JOURNAL</el-menu-item>
              <el-menu-item index="/KITTENS">KITTENS</el-menu-item>
              <el-menu-item index="/TRAVEL">TRAVEL</el-menu-item>
            </el-submenu>
            <el-menu-item index="/CONTACT">CONTACT</el-menu-item>
          </el-menu>
        </div>
        <div class="content">
          <el-row :gutter="20">
            <el-col :span="4" class="content-left">
              <div class="contact" style="background-color: #a2c7d5"  onclick="window.open('mailto:yyid404@gmail.com');">
                <svg t="1596450705414" class="contact-icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="1550"><path d="M32 416v544h960V416L512 32z" fill="#FFF5E8" p-id="1551"></path><path d="M32 416v544h960V416L512 768z" fill="#FFC5CB" p-id="1552"></path><path d="M32 960h960L512 576z" fill="#FF9DAC" p-id="1553"></path><path d="M539.776 284.16a118.016 118.016 0 0 1 166.784 0 118.08 118.08 0 0 1 0 166.752L512 645.472l-194.56-194.56a118.016 118.016 0 0 1 0-166.752 118.08 118.08 0 0 1 166.784 0l27.776 27.776 27.776-27.776z" fill="#F83B57" p-id="1554"></path></svg>
              </div>
              <div class="contact" style="background-color: #b3d3df" onclick="window.open('https://github.com/yyid404');">
                <svg t="1596454567186" class="contact-icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="13594" width="200" height="200"><path d="M427.392 853.504a61.44 61.44 0 0 1-1.450667 15.530667 92.586667 92.586667 0 0 1-10.965333 27.605333c-15.061333 25.301333-40.661333 42.154667-73.642667 42.154667-77.653333 0-108.117333-38.101333-146.261333-133.504C169.216 740.693333 157.013333 725.461333 128 725.461333v-85.333333c77.653333 0 108.117333 38.101333 146.261333 133.504 25.856 64.597333 38.058667 79.786667 67.072 79.786667 0-12.373333-0.170667-23.296-0.512-38.144-0.853333-34.816-0.938667-41.941333 0.554667-51.2 0.64-20.352 5.888-34.773333 16.384-49.066667-95.232-20.736-159.445333-63.573333-196.309333-132.992l-13.824-32.426667C134.186667 510.848 128 467.072 128 416.426667c0-58.24 17.749333-110.336 50.944-153.856-10.368-41.386667-8.96-91.989333 13.909333-149.077334l7.466667-18.688 19.2-6.101333c2.56-0.853333 5.632-1.578667 9.301333-2.133333 37.290667-5.888 90.325333 8.106667 159.701334 52.48a565.930667 565.930667 0 0 1 127.274666-14.208c38.741333 0 77.226667 3.882667 114.048 11.605333 67.456-42.24 119.04-55.509333 155.306667-49.92 3.626667 0.597333 6.741333 1.322667 9.258667 2.133333l19.285333 6.101334 7.466667 18.773333c20.010667 50.218667 23.424 96.469333 16.128 136.96C875.434667 296.32 896 352.597333 896 416.512c0 53.888-3.84 94.378667-14.933333 133.802667l-11.733334 32.170666c-30.677333 69.333333-98.304 112.64-202.538666 133.248 10.837333 15.018667 15.872 30.250667 15.872 52.394667v42.666667l-0.042667 42.666666a13.013333 13.013333 0 0 0 0.341333 2.730667L682.666667 938.794667c-36.352 0-63.36-17.706667-76.672-45.653334a88.277333 88.277333 0 0 1-8.661334-40.277333v-84.736c0-3.584-0.128-3.797333-8.832-12.501333-23.296-23.296-33.834667-40.874667-33.834666-72.832v-38.613334l38.4-3.84c114.346667-11.52 176.512-43.221333 197.12-89.6l9.6-26.325333c7.68-27.562667 10.88-61.098667 10.88-107.946667 0-49.706667-17.365333-90.837333-50.218667-123.648L742.4 274.773333l7.381333-24.448c6.528-21.717333 8.106667-47.402667 1.152-76.714666a158.634667 158.634667 0 0 0-3.584 0.938666c-22.826667 6.4-51.370667 20.053333-85.76 43.008l-15.658666 10.453334-18.304-4.522667a467.754667 467.754667 0 0 0-111.829334-13.269333c-42.709333 0-84.906667 5.418667-123.946666 16.042666l-19.029334 5.205334-16.256-11.136c-35.541333-24.32-65.109333-38.826667-88.746666-45.568a158.293333 158.293333 0 0 0-4.864-1.28c-8.234667 33.92-4.992 61.781333 3.413333 82.688l9.984 25.088-18.346667 19.797333C228.693333 332.629333 213.333333 370.986667 213.333333 416.512c0 41.685333 4.864 76.202667 13.824 102.229333l11.178667 26.453334c27.904 52.352 87.168 83.84 192.853333 95.146666l38.144 4.096v38.357334c0 32-10.538667 49.536-33.834666 72.832-8.704 8.704-8.832 8.96-8.832 12.501333l-0.725334 7.893333c-0.512 2.56-0.512 9.258667 0.170667 37.205334 0.298667 12.8 0.469333 22.997333 0.554667 33.621333a33.962667 33.962667 0 0 1 0.725333 6.656z" p-id="13595" fill="#ffffff"></path></svg>
              </div>
              <div class="contact" id="wechat" style="background-color: #c4dde7">
                <svg t="1596450861957" class="contact-icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="10200"><path d="M554.666667 512a42.666667 42.666667 0 0 1 42.666666 42.666667v21.333333a42.666667 42.666667 0 1 1-85.333333 0V554.666667a42.666667 42.666667 0 0 1 42.666667-42.666667zM725.333333 512a42.666667 42.666667 0 0 1 42.666667 42.666667v21.333333a42.666667 42.666667 0 1 1-85.333333 0V554.666667a42.666667 42.666667 0 0 1 42.666666-42.666667z" fill="#ffffff" p-id="10201"></path><path d="M298.666667 597.333333a298.666667 298.666667 0 0 1 298.666666-298.666666h85.333334a298.666667 298.666667 0 0 1 243.242666 472.021333l12.416 98.645333a42.666667 42.666667 0 0 1-53.845333 46.421334l-115.541333-32.426667A298.581333 298.581333 0 0 1 682.666667 896h-85.333334a298.666667 298.666667 0 0 1-298.666666-298.666667z m298.666666-213.333333a213.333333 213.333333 0 0 0 0 426.666667h85.333334c25.002667 0 48.938667-4.266667 71.125333-12.117334a42.666667 42.666667 0 0 1 25.728-0.853333l66.133333 18.517333-6.570666-52.181333a42.666667 42.666667 0 0 1 9.216-32.213333A213.333333 213.333333 0 0 0 682.666667 384h-85.333334z" fill="#ffffff" p-id="10202"></path><path d="M42.666667 448A362.666667 362.666667 0 0 1 405.333333 85.333333h128a361.856 361.856 0 0 1 270.293334 120.874667 42.666667 42.666667 0 0 1-63.573334 56.917333A276.522667 276.522667 0 0 0 533.333333 170.666667h-128a277.333333 277.333333 0 0 0-184.874666 484.053333 42.666667 42.666667 0 0 1 13.610666 39.04l-9.301333 54.058667 39.168-12.970667a42.666667 42.666667 0 1 1 26.794667 81.066667l-106.666667 35.242666a42.666667 42.666667 0 0 1-55.466667-47.701333l17.493334-101.802667A361.6 361.6 0 0 1 42.666667 448z" fill="#ffffff" p-id="10203"></path></svg>
                <div>
                  <img class="code" src="https://myblog-pics.oss-cn-shenzhen.aliyuncs.com/user/user-wechat-Lemon.png"/>
                </div>
              </div>
              <div class="contact" style="background-color: #d1e5ed" onclick="window.open('https://www.instagram.com/yyid404/');">
                <svg t="1596454626429" class="contact-icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="14489" width="200" height="200"><path d="M658.285714 512q0-60.571429-42.857143-103.428571t-103.428571-42.857143-103.428571 42.857143-42.857143 103.428571 42.857143 103.428571 103.428571 42.857143 103.428571-42.857143 42.857143-103.428571z m78.857143 0q0 93.714286-65.714286 159.428571t-159.428571 65.714286-159.428571-65.714286-65.714286-159.428571 65.714286-159.428571 159.428571-65.714286 159.428571 65.714286 65.714286 159.428571z m61.714286-234.285714q0 21.714286-15.428572 37.142857t-37.142857 15.428571-37.142857-15.428571-15.428571-37.142857 15.428571-37.142857 37.142857-15.428572 37.142857 15.428572 15.428572 37.142857zM512 152q-4 0-43.714286-0.285714t-60.285714 0-55.142857 1.714285-58.857143 5.714286T253.142857 169.714286q-28.571429 11.428571-50.285714 33.142857t-33.142857 50.285714q-6.285714 16.571429-10.571429 40.857143t-5.714286 58.857143-1.714285 55.142857 0 60.285714 0.285714 43.714286-0.285714 43.714286 0 60.285714 1.714285 55.142857 5.714286 58.857143T169.714286 770.857143q11.428571 28.571429 33.142857 50.285714t50.285714 33.142857q16.571429 6.285714 40.857143 10.571429t58.857143 5.714286 55.142857 1.714285 60.285714 0 43.714286-0.285714 43.714286 0.285714 60.285714 0 55.142857-1.714285 58.857143-5.714286 40.857143-10.571429q28.571429-11.428571 50.285714-33.142857t33.142857-50.285714q6.285714-16.571429 10.571429-40.857143t5.714286-58.857143 1.714285-55.142857 0-60.285714-0.285714-43.714286 0.285714-43.714286 0-60.285714-1.714285-55.142857-5.714286-58.857143T854.285714 253.142857q-11.428571-28.571429-33.142857-50.285714t-50.285714-33.142857q-16.571429-6.285714-40.857143-10.571429t-58.857143-5.714286-55.142857-1.714285-60.285714 0-43.714286 0.285714z m438.857143 360q0 130.857143-2.857143 181.142857-5.714286 118.857143-70.857143 184t-184 70.857143q-50.285714 2.857143-181.142857 2.857143t-181.142857-2.857143q-118.857143-5.714286-184-70.857143T76 693.142857q-2.857143-50.285714-2.857143-181.142857t2.857143-181.142857q5.714286-118.857143 70.857143-184t184-70.857143q50.285714-2.857143 181.142857-2.857143t181.142857 2.857143q118.857143 5.714286 184 70.857143t70.857143 184q2.857143 50.285714 2.857143 181.142857z" p-id="14490" fill="#ffffff"></path></svg>
              </div>
              <div class="contact" style="background-color: #e3eff3" onclick="window.open('https://weibo.com/8oz3yy');">
                <svg t="1596450915873" class="contact-icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="11913"><path d="M916.402423 396.448264c-21.263279 0-38.503942-17.238616-38.503942-38.503942 0-85.059258-68.954465-154.015769-154.013723-154.015769-21.265326 0-38.505989-17.238616-38.505989-38.503942 0-21.263279 17.23964-38.503942 38.505989-38.503942 127.58991 0 231.021607 103.434767 231.021607 231.023654C954.906365 379.209648 937.667749 396.448264 916.402423 396.448264zM718.357881 490.670206c52.093449 32.000831 82.757842 82.790588 82.757842 141.093459 0 128.125099-151.514809 265.314645-377.066845 265.314645-84.021625 0-165.42768-20.435425-229.246171-57.567113C113.742531 792.356222 69.093635 722.702839 69.093635 643.419122c0-78.041424 41.922808-161.346735 121.272018-240.930281 75.992765-76.162634 162.956396-121.632221 232.631268-121.632221 47.340191 0 77.138868 19.910469 93.739964 36.566824 9.119705 9.126868 20.155039 23.246447 27.656897 43.213197 11.279904-1.568728 22.203698-2.367931 32.637328-2.367931 70.069869 0 104.813161 34.790364 119.271454 55.499012C708.334597 431.008384 719.522404 456.407867 718.357881 490.670206zM643.810025 541.012777c-9.342786-2.800789-15.736403-4.718465-10.848069-17.014512 10.585079-26.677593 11.675924-49.708122 0.207731-66.122977-10.679223-15.303544-30.570249-22.597671-56.138578-22.597671-25.926486 0-57.719586 7.498788-91.671862 21.75242-0.038886 0-5.865591 2.547009-10.603499 2.547009-4.307096 0-7.747451-2.096754-5.170766-10.105149 10.380418-33.42732 8.81783-61.45977-7.330966-77.628008-9.458419-9.485025-22.975271-13.978363-39.257096-13.978363-46.721091 0-116.226095 36.990472-178.118724 99.015108-62.492286 62.680575-98.777701 129.10338-98.777701 186.53951 0 109.872387 140.496871 176.652326 277.95043 176.652326 180.204222 0 300.05896-104.965633 300.05896-188.30676C724.107839 581.39551 681.807431 552.819684 643.810025 541.012777zM743.136218 357.944322c0-10.633175-8.621355-19.25146-19.25146-19.25146-21.265326 0-38.505989-17.238616-38.505989-38.501896 0-21.265326 17.23964-38.505989 38.505989-38.505989 50.503231 0 91.460038 39.029922 95.476515 88.50166 0.511653 2.5071 0.781806 5.102205 0.781806 7.758708 0 21.265326-17.238616 38.503942-38.503942 38.503942C760.374834 396.448264 743.136218 379.209648 743.136218 357.944322z" p-id="11914" fill="#ffffff"></path></svg>
              </div>
            </el-col>
            <el-col :span="10" class="content-right">
              <el-form ref="form" :model="form" label-width="80px">
                <el-form-item label="Nickname">
                  <el-input v-model="form.name"></el-input>
                </el-form-item>
                <el-form-item label="Telephone">
                  <el-input v-model="form.telephone"></el-input>
                </el-form-item>
                <el-form-item label="Email">
                  <el-input v-model="form.email"></el-input>
                </el-form-item>
                <el-form-item label="Message">
                  <el-input type="textarea" v-model="form.content"></el-input>
                </el-form-item>
                <el-form-item>
                  <el-button type="primary" @click="onSubmit">Submit</el-button>
<!--
                  <el-button>Cancel</el-button>
-->
                </el-form-item>
              </el-form>
            </el-col>
          </el-row>
        </div>
        <el-footer height="30px">分页</el-footer>
      </div>
    </el-container>
  </div>
</template>

<script>
  export default {
    name: 'Contact111',
    data () {
      return {
        circleUrl: "https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png",
        squareUrl: "https://myblog-pics.oss-cn-shenzhen.aliyuncs.com/user/user-avatar-Lemon.jpg",
        activeIndex2: '1',
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
        }
      }
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      },
      onSubmit() {
        console.log('submit!');
      }
    }
  }
</script>
<style scoped>
  .container{
    background-color: #f1f5f6;
  }

  .el-header {
    background-image: url("https://myblog-pics.oss-cn-shenzhen.aliyuncs.com/background/theme-banner-daily-1.jpg");
    background-size: auto 100%;
    line-height: 0px;
  }

  .margin-top{
    height: 20px;
  }

  .el-row {
    margin-bottom: 20px;
  }

  .demo-avatar{
    width: 100px;
    margin: 0 auto 20px auto;
  }
  .nickname{
    color: whitesmoke;
    text-align: center;
    height: 25px;
  }
  .introduce{
    font-size: 12px;
    color: whitesmoke;
    text-align: center;
  }

  .container-content{
    background-image: url("https://myblog-pics.oss-cn-shenzhen.aliyuncs.com/background/theme-background-daily-3.jpg");
    background-size: 450px;
  }

  .menu{
    background-color: #73aec4;
    opacity: 70%;
    display:flex;
    justify-content:center;
  }

  .content{
    height: 350px;
  }

  .content-left{
  }

  .content-right{
    margin-top: 20px;
    margin-left: 10%;
  }

  .contact{
    width: 70px;
    height: 70px;
  }

  .contact:hover{
    opacity: 90%;
  }

  .code{
    width: 100px;
    height: 100px;
    margin-left: 70px;
  }

  #wechat > div img {               /*子代选择器*/
    visibility: hidden;
    position: absolute;
    transition: visibility .2s ease,top .4s ease; /*设置过渡属性*/
    z-index: -1;
    top: 0px;
  }
  #wechat:hover >div img {
    visibility: visible;
    top: 125px;
  }

  .contact-icon{
    width: 40px;
    height: 40px;
    margin-left: 15px;
    margin-top: 15px;
  }

  .el-footer {
    background-color: #73aec4;
    color: #f9f177;
    text-align: center;
    line-height: 30px;
    /*
        position: fixed;
    */
    bottom: 0px;
    width: 100%;
    opacity: 70%;
  }
</style>
