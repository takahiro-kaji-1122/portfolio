<template>
  <div class="app">
    <div id="Drawer">
      <Drawer />
    </div>
    <!--<div>{{ this.skills }}</div>-->
    <div id="Main">
      <Main />
    </div>
    <div id="About">
      <About />
    </div>
    <div id="Skill">
      <Skill />
    </div>
    <div id="Vision">
      <Vision />
    </div>
    <div id="Footer">
      <Footer />
    </div>
    <!-- test
    ボタン切り替え
      <div id="app">
      {{ message }}
</div>
     test -->
  </div>
</template>

<script>
import Drawer from './components/Menu.vue'
import Main from './components/Main.vue'
import About from './components/About.vue'
import Skill from './components/Skill.vue'
import Vision from './components/Vision.vue'
import Footer from './components/footer.vue'


export default {
  name: 'App',
  components: {
    Drawer,
    Main,
    About,
    Skill,
    Vision,
    Footer
  },
  mounted(){
    this.$store.dispatch('updateSkillScores');
  },
/*data() {
    return {
      skills: []
    }
  },
  mounted () {
    this.getSkills();
  },
  methods: {
    getSkills() {
      // dataのスキルを初期化する
      this.skills = [];
      // this.skillsを一時変数のitemsに参照コピーする
      let items = this.skills;
      // axios.getを用いてデプロイ済のfunctionにアクセスする
      this.axios.get('https://us-central1-portfolio-12283.cloudfunctions.net/skills')
        .then((response) => {
          response.data.forEach(function(skill) {
            // 取得したデータを１件ずつ配列に設定する
            items.push(skill);
          })
        })
        .catch((e) => {
          alert(e);
        });
        console.log(items)
    }
  }
*/
}



/*
test
ボタン切り替え
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
↑test
*/
</script>

<style scoped>


#app {
  display: inline-block;
  text-align: center;
}

</style>
