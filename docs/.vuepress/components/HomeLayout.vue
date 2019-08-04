<template>
  <div class="home-layout">
    <div class="content">
      <div class="content-header">
        <ul class="left-spot">
          <li class="red"></li>
          <li class="yellow"></li>
          <li class="green"></li>
        </ul>
        <span>斜杠青年工作室</span>
      </div>
      <div class="content-inner">
        <ul id="info" class="info-ul">
          <li>Welcome to 斜杠青年工作室</li>
          <li>-> ~ cd slashYouthStudio</li>
          <li>-> <span>slashYouthStudio</span>Thanks for your visit, let me introduce myself.</li>
          <li>-> <span>slashYouthStudio</span><div class="text-kuai">Name：</div>鲍小帅</li>
          <li>-> <span>slashYouthStudio</span><div class="text-kuai">Sex：</div>man</li>
          <li>-> <span>slashYouthStudio</span><div class="text-kuai">Age：</div>25</li>
          <li>-> <span>slashYouthStudio</span><div class="text-kuai">Address：</div>BeiJing</li>
          <li>-> <span>slashYouthStudio</span><div class="text-kuai">Job：</div>WEB Engineer</li>
          <li>-> <span>slashYouthStudio</span><div class="text-kuai">Email：</div>baoshuaipeng@163.com</li>
          <li>-> <span>slashYouthStudio</span>Ok is done</li>
          <li>-> <span>slashYouthStudio</span>Now. you can visit my blog! </li>
          <li>-> <span>slashYouthStudio</span>Choose one you want to go!</li>
          <li>-> <span>slashYouthStudio</span><a href="/dier">BlogHomePage</a></li>
          <li>-> <span>slashYouthStudio</span><a href="/dier">Photo</a></li>
          <li>-> <span>slashYouthStudio</span><a href="/dier">Article</a></li>
          <li>-> <span>slashYouthStudio</span><a href="/dier">Tag</a></li>
          <li class="is-ali">
            😝
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      
    }
  },
  methods: {
    makeOut() {
      let _infoUl= document.getElementById('info')
      for (var i=0; i< _infoUl.childNodes.length; i++) {
        (function (i) {
          setTimeout(() => {
            if(_infoUl.childNodes[i].nodeName != '#text') {
              _infoUl.childNodes[i].style.display = "flex"
            }
          }, 200 * i)
        })(i)
      }
    }
  },
  mounted() {
    this.$nextTick(function () {
      this.makeOut()
    })
  },
}
</script>


<style>
*{
  box-sizing: border-box;
  list-style: none;
  margin: 0px;
  padding: 0px;
}
div{
  box-sizing: border-box;
  position: relative;
}
.home-layout{
  width: 100vw;
  height: 100vh;
  background: linear-gradient(-90deg,#9c9a9a 10%,#4b4747 90%);
  display: flex;
  justify-content: center;
  padding-top: 50px;
}
.content{
  width: 990px;
  height: 680px;
  box-shadow: -2px 7px 20px 3px #222;
}
.content-header{
  width: 100%;
  height: 34px;
  background-color: #222;
  text-align: center;
  padding: 2px;
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
  color: #fff;
  text-shadow: #a09c9b 0 0 1px, #fffffb 0 0 1px, #fffffb 0 0 1px;
  -webkit-box-shadow: inset 0 3px 20px 0 #414141;
  box-shadow: inset 0 3px 20px 0 #414141;
}
.content-inner{
  padding-top: 50px;
  background-color: #313131;
  height: calc(100% - 34px);
  padding: 20px;
  font-weight: 400;
  font-family: Fira Code,Source Code Pro,Monaco,Menlo,Consolas,monospace;
  color: #fff;
  text-shadow: #a09c9b 0 0 1px, #fffffb 0 0 1px;
  font-size: 13px;
}
.left-spot{
  position: absolute;
  left: 0;
  top: 0;
}
.left-spot>li{
  display: inline-block;
  width: 12px;
  height: 12px;
  border-radius: 6px;
  margin-left: 6px; 
}
.red{
  background-color: #c83030;
}
.yellow{
  background-color: #f7db60;
}
.green{
  background-color: #2ec971
}
.text-kuai{
  padding: 2px 3px;
  background: #2980b9;
  margin-right: 5px;
}
.info-ul{
  width: 100%;

}
.info-ul>li{
  display: flex;
  align-items: center;
  height: 35px;
  display: none;
}
.info-ul>li>span{
  color: #0fff95;
  margin-right: 10px;
  margin-left: 6px;
}
.info-ul>li>a{
  color: #fffbbd;
  text-decoration: underline;
}
.info-ul>li:last-child{
  font-size: 24px;
  height: 60px;
}




</style>
