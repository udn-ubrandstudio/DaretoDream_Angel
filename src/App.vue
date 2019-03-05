<template>
  <div id="app">
    <indicator></indicator>
    <div class="cover" :style="{'background-image': 'url(' + srcRWD(cover, coverWeb) + ')' }" ref="beginning">
      <div class="cover-title">
        <h3>
          征服殘酷街頭<br>Angel：要把心中音樂帶給世界
        </h3>
      </div>
    </div>
    <div class="back-to-home" ref="home" :class="{ 'hidden-home' : isShowHome }">
      <a class="home" href="https://dc.udn.com/nereus/TEK1903F0001/DaretoDream/index.html">
        <img :src="srcRWD(home, homeWeb)" alt="">
        HOME
      </a>
    </div>
    <br>
    <content-container>
      <div>
        <share href="https://udn.com/upf/ubrand/2019_data/DaretoDream_BR/index.html"></share>
      </div>
      <br>
      <div class="title-track-same-month">
         <youtube src="https://www.youtube.com/embed/i035D6GbHWo"></youtube>
      </div>
      <br>
      <p>站上街頭表演難不難？得面對一雙雙陌生眼光，幸運的話有人駐足或打賞，但大多數人是冷漠的。身為一名街頭藝人，每天都必須比昨天更努力，才有獲得掌聲的機會。</p>
      <br>
      <p>你可能在信義區、淡水街頭聽過她的琴聲，她叫Angel，人如其名，留著烏黑長髮，每首曲子結束時總報以觀眾一抹甜笑。談起當初放棄律師考試時爸媽的反應，「我只記得媽媽說她栽培我4年念完法律系，我的決定讓她很心痛。」Angel爸爸更認為街頭藝人會喝酒吸毒，得不到家人肯定和支持，讓她長達半年幾乎不敢回家。</p>
      <br>
      <br>
      <column-one description="外表看似嬌弱的Angel，拉起琴又是另一種堅毅模樣。" src="@/../static/pic1.png" src-web="@/../static/pic1_web.png"></Column-One>
      <br>
      <h3>人生只有一次　<br class="mobile-only">要做就要全力以赴</h3>
      <br>
      <p>高中念中山女中，大學是北大法律系，Angel自小就被歸類為會讀書的乖乖牌，父母對她期望甚高。問她為何想當街頭藝人？Angel說：「雖然我個性感覺好像乖乖、靜靜的，但其實我是一個蠻喜歡挑戰跟變化的人。」拉小提琴一直是她讀書時期紓壓的方式，大學畢業為了律師考試的費用，開始嘗試去街頭表演。</p>
      <br>
      <p>Angel回憶第一次表演，「那是個很冷的冬天，我心裡很害怕，拉琴時手一直抖，呼吸都快呼不上來。」但也是這次表演在她心底種下夢想的嫩芽，「當時有個媽媽帶著小孩，走過來跟我說『加油，我相信妳一定會成功的』，她是第一個打賞我的人，我一直印象很深刻。」</p>
      <br>
      <p>緊張和憂慮沒有讓Angel裹足不前，只花一星期就上場表演，對她來說機會稍縱即逝，想到的當下就得立刻去做。在街頭遇見的這些人，也讓她堅信音樂有魔力，能為自己及他人帶來快樂與美好。</p>
      <br>
      <br>
      <column-one description="Angel在維也納街頭表演，沒有孤獨，只有更靠近夢想的雀躍。" src="@/../static/pic2.png" src-web="@/../static/pic2_web.png"></Column-One>
      <br>
      <h3>勇闖國外表演　<br class="mobile-only">被警察趕是日常</h3>
      <br>
      <p>街頭是殘酷的，因為不是從小學琴，Angel也曾遇過有人說「拉這樣怎麼還敢出來拉琴？」自尊心高的她沒有受打擊，反而更常去找老師練琴，一周有4、5天去街頭表演，也接商演、婚禮表演，更曾獨自到澳洲、美國、加拿大和歐洲表演。在國外很多地方無法申請街頭藝人證照，被警察趕更是日常，也遇過有人把她的打賞金全拿走，這些在異鄉的磨練，促使Angel更堅定，一步步實踐「將音樂分享給世界」的夢想。</p>
      <br>
      <br>
      <column-one description="家中簡單的桌椅，是Angel平日找曲子、練譜的地方。" src="@/../static/pic3.png" src-web="@/../static/pic3_web.png"></Column-One>
      <br>
      <h3>難過的情緒會過去　<br class="mobile-only">找到自我信念很重要</h3>
      <br>
      <p>很多人會說，街頭藝人養得活自己嗎？的確，光淡水老街就有近40個街頭藝人爭搶4、5個位子，對現在的Angel來說，金錢是維持夢想的必要，但不是表演的最終目的。生活寡慾的她，家中只有一張桌子和椅子，平常不是在練琴，就是在找曲子。她追夢的信念是：「保持樂觀的心、不斷自我檢討，記住讓自己感動的時刻。」只要能每天帶著熱愛的小提琴，把心中音樂帶上街頭，就是Angel最大的滿足。</p>
      <br>
      </content-container>
      <content-container class="web-only" style="background-image: linear-gradient(to bottom, #f2f2f2, rgba(255, 255, 255, 0)); ">
      <div class="anchor-web">
        <h3 class="anchor-web-title">點看其他人物故事</h3>
        <ul>
          <li v-for="item in profiles" :key="item.id" :class="{ shake: item.isLock }">
            <a :href="item.link">
              <img :src="item.profile_web"  @click="handleLinkTo(item.isLock, item.idTo, $event)" alt="">
              <div class="describe">
                <p>{{ item.title }}</p>
                <p>{{ item.name }}</p>
             </div>
            </a>
          </li>
        </ul>
      </div>
      </content-container>
      <div class="anchor-mobile">
        <h3 class="anchor-mobile-title">點看其他人物故事</h3>
        <ul>
          <li v-for="item in profiles" :key="item.id" :class="{ shake: item.isLock }">
            <a :href="item.link">
              <img :src="item.profile"  @click="handleLinkTo(item.isLock, item.idTo, $event)" alt="">
              <div class="describe">
                <p>{{ item.title }}</p>
                <p>{{ item.name }}</p>
             </div>
            </a>
          </li>
        </ul>
      </div>
      <content-container>
      <br>
      <div class="share-and-logo">
        <div class="share">
          <share href="https://udn.com/upf/ubrand/2019_data/DaretoDream_BR/index.html"></share>
        </div>
        <div class="logo">
          <logo use-ubrand="yes" use-vision='no'>
            <div>
              <img :src="logo" alt="">
            </div>
          </logo>
        </div>
      </div>
      <p><br></p>
      <editor>
        <div>文字採訪：盧巧梅</div>
        <div>影音製作：劉宜峰</div>
        <div>視覺設計：呂宗原</div>
        <div>網頁製作：吳偉賢</div>
        <div>議題行銷：張乃文、陳欣媛、王敏霏</div>
        <div>監製：董谷音、蔡幸怡、陳曼薇、蕭銘志</div>
        <div>2019.3.15</div>
      </editor>
      <p><br></p>
      <fb-comment href="https://udn.com/upf/ubrand/2019_data/DaretoDream_BR/index.html"></fb-comment>
    </content-container>
    <back-top></back-top>
    <back-home></back-home>
    <foot></foot>
  </div>
</template>

<script>
import Vue from 'vue'
import srcRWD from '@/mixin/srcRWD.js'
import globalComponents from '@/plugins/baseComponents.js'
import videoBox from '@/components/videoBox.vue'
import backHome from '@/components/backHome.vue'

Vue.use(globalComponents)

export default {
  name: 'App',
  mixins: [srcRWD],
  components: {
    videoBox,
    backHome
  },
  data () {
    return {
      isShowHome: false,
      cover: require('@/../static/cover.png'),
      coverWeb: require('@/../static/cover_web.png'),
      logo: require('@/../static/logo.png'),
      home: require('@/../static/home.png'),
      homeWeb: require('@/../static/homeWeb.png'),
      profiles: [
      {
        id: 'duncan_btn',
        idTo: 'duncan',
        title: '圖文創作者',
        name: 'Duncan',
        profile: require('@/../static/profiles/duncan.png'),
        profile_web: require('@/../static/profiles/duncan_web.png'),
        link: 'https://udn.com/upf/ubrand/2019_data/DaretoDream_Duncan/index.html',
        isLock: false
      },
      {
        id: 'br_btn',
        idTo: 'br',
        title: '饒舌歌手',
        name: 'BR',
        profile: require('@/../static/profiles/br.png'),
        profile_web: require('@/../static/profiles/br_web.png'),
        link: 'https://udn.com/upf/ubrand/2019_data/DaretoDream_BR/index.html',
        isLock: false
      },
      {
        id: 'angel_btn',
        idTo: 'angel',
        title: '小提琴手',
        name: 'Angel',
        profile: require('@/../static/profiles/angel.png'),
        profile_web: require('@/../static/profiles/angel_web.png'),
        link: 'https://dc.udn.com/nereus/TEK1903F0001/DaretoDream_Angel/index.html',
        isLock: false
      },
      {
        id: 'anonymous2_btn',
        idTo: 'anonymous2',
        title: '4月',
        name: '即將推出',
        profile: require('@/../static/profiles/lock.png'),
        profile_web: require('@/../static/profiles/lock_web.png'),
        link: '.',
        isLock: true
      },
      {
        id: 'anonymous3_btn',
        idTo: 'anonymous3',
        title: '5月',
        name: '即將推出',
        profile: require('@/../static/profiles/lock.png'),
        profile_web: require('@/../static/profiles/lock_web.png'),
        link: '.',
        isLock: true
      },
      {
        id: 'anonymous4_btn',
        idTo: 'anonymous4',
        title: '6月',
        name: '即將推出',
        profile: require('@/../static/profiles/lock.png'),
        profile_web: require('@/../static/profiles/lock_web.png'),
        link: '.',
        isLock: true
      }]
    }
  },
  methods: {
    handleLinkTo (isLock ,idTo ,event) {

      let label = "[DaretoDream_BR][" + idTo + "][外連到" + idTo + "]"

      if(isLock) {
        label = "[DaretoDream_BR][" + idTo + "][目前無法外連]"
        event.preventDefault()
      }

      window.ga("send", {
        "hitType": "event",
        "eventCategory": "OptionButton",
        "eventAction": "click",
        "eventLabel": label
      })
    },
    handle_scroll () {
      let currentHeight = window.pageYOffset
      if (currentHeight > 0) {
        this.isShowHome = true
      } else {
        this.isShowHome = false
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handle_scroll)
  },
  destroyed () {
    window.removeEventListener('scroll', this.handle_scroll)
   }
}
</script>

<style  lang="scss">
@import './assets/CSS/theme.css';
@import './assets/CSS/UdnFontSize.css';

html, body {
  margin: 0;
  padding: 0;
}
#app {
    font-family: Microsoft JhengHei;
    .web-only {
      @media screen and (max-width: 768px) {
        display: none;
      }
      @media screen and (min-width: 768px) and (max-width: 1023px) {
          display: none;
      }
    }
    .mobile-only {
      @media screen and (min-width: 768px) and (max-width: 1023px) {
        display: none;
      }
      @media screen and (min-width: 1024px) {
        display: none;
      }
    }
    .cover {
      position: relative;
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
      height: 100vh;
      .main-cover {
        width: 100%;
      }
      .cover-title {
        width: 100%;
        background-color: rgba(#e60414, 0.6);
        position: absolute;
          bottom: 110px;
          left: 0;
        @media screen and (min-width: 768px) and (max-width: 1023px) {
          bottom: 0;
        }
        @media screen and (min-width: 1024px) {
          bottom: 0;
        }
        h3 {
          margin: 0px;
          padding: 9px 15px 12px 15px;
          color: white;
          font-weight: bolder;
          @media screen and (min-width: 768px) and (max-width: 1023px) {
            font-size: 5vw;
            padding: 9px 50px 12px 50px;
          }
          @media screen and (min-width: 1024px) {
            font-size: 5vw;
            padding: 9px 50px 12px 50px;
          }
        }
      }
    }
    .back-to-home {
      width: 48px;
      height: 47px;
      background-color: #e60414;
      border-radius: 51% 0 0 51%;
      padding: 10px;
      position: fixed;
      right: 0;
      bottom: 10vh;
      z-index: 100;
      font-size: 9px;
      white-space: nowrap;
      cursor: pointer;
      display: flex;
      align-items: center;
      transform: translateX(100%);
      opacity: 0;
      transition: all 1s;
      font-weight: 900;
      @media screen and (min-width: 768px) and (max-width: 1023px) {
        display: none;
      }
      @media screen and (min-width: 1024px) {
        display: none;
      }
      a {
        color: white;
        cursor: pointer;
        width: 100%;
        height: 100%;
        img {
          display: block;
          width: 9px;
          position: relative;
          left: 50%;
          transform: translate(-25%);
        }
      }
    }
    .hidden-home {
      transform: translateX(0%);
      opacity: 1;
    }
   .anchor-web {
      @media screen and (max-width: 768px) {
        display: none;
      }
      .anchor-web-title {
        padding: 21px 0 55px 0;
        font-size: 37.9px;
        font-weight: bold;
        text-align: center;
      }
      ul {
        display: flex;
        justify-content: space-around;
        margin:0;
        padding: 0;
        text-indent: 0;
        list-style-type: 0;
        li {
          overflow: hidden;
          height: auto;
          width: 110px;
          display: flex;
          align-items: center;
          justify-content: center;
          flex-direction: column;
          position: relative;
          a {
            text-decoration: none;
            color: black;
            width: 100%;
          }
          img {
            width: 100%;
            cursor: pointer;
            border-radius: 51%;
          }
          p {
            margin: 0;
            line-height: 1;
            text-align: center;
            font-size: 17px;
            line-height: 1.35;
            font-weight: bolder;
          }
          .locked {
            background-color: gray;
            width: 100%;
            height: 100%;
            position: absolute;
          }
        }
        .shake:hover, .shake:active {
            animation: shake 0.82s cubic-bezier(.36,.07,.19,.97) both;
            transform: translate3d(0, 0, 0);
            backface-visibility: hidden;
            perspective: 1000px;
          }
          @keyframes shake {
            10%, 90% {
              transform: translate3d(-1px, 0, 0);
            }

            20%, 80% {
              transform: translate3d(2px, 0, 0);
            }

            30%, 50%, 70% {
              transform: translate3d(-4px, 0, 0);
            }

            40%, 60% {
              transform: translate3d(4px, 0, 0);
            }
          }
      }
    }
   .anchor-mobile {
     background-image: linear-gradient(to bottom, #f2f2f2, rgba(255, 255, 255, 0));
     padding-bottom: 13px;
      @media screen and (min-width: 1024px) {
        display: none;
      }
      .anchor-mobile-title {
        padding: 25px 0;
        font-size: 25px;
        font-weight: 900;
        text-align: center;
        color: black;
        margin: 0;
        text-align: center;
      }
      ul {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        margin:0;
        padding: 0;
        text-indent: 0;
        list-style-type: 0;
        li {
          overflow: hidden;
          width: 30%;
          display: flex;
          align-items: center;
          justify-content: center;
          position: relative;
          margin: 5px 0;
          flex-direction: column;
          text-align: center;
          @media screen and (min-width: 768px) and (max-width: 1023px) {
            width: 15%;
            height: auto;
          }
          a {
            width: 100%;
            text-decoration: none;
            color: black;
          }
          img {
            width: 75%;
            cursor: pointer;
            border-radius: 51%;
            margin: 5px;
          }
          p {
            margin: 0;
            line-height: 1;
            text-align: center;
            font-size: 12px;
            line-height: 1.33;
            font-weight: bolder;
          }
          .locked {
            background-color: gray;
            width: 100%;
            height: 100%;
            position: absolute;
          }
        }
        .shake:hover, .shake:active {
            animation: shake 0.82s cubic-bezier(.36,.07,.19,.97) both;
            transform: translate3d(0, 0, 0);
            backface-visibility: hidden;
            perspective: 1000px;
          }
          @keyframes shake {
            10%, 90% {
              transform: translate3d(-1px, 0, 0);
            }

            20%, 80% {
              transform: translate3d(2px, 0, 0);
            }

            30%, 50%, 70% {
              transform: translate3d(-4px, 0, 0);
            }

            40%, 60% {
              transform: translate3d(4px, 0, 0);
            }
          }
      }
    }
    .share-and-logo {
      display: flex;
      justify-content: flex-start;
      flex-direction: column;
      @media (min-width: 768px) and (max-width: 1024px){
        justify-content: space-between;
        flex-direction: row;
      }
      @media screen and (min-width: 1025px){
        justify-content: space-between;
        flex-direction: row;
      }
      .share {
        min-width: 35%;
      }
      .logo {
        @media (min-width: 768px) and (max-width: 1024px){
          margin-top: -5px;
        }
        @media screen and (min-width: 1025px){
          margin-top: -5px;
        }
      }
    }
}
</style>
