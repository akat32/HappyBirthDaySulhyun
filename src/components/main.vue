<template>
  <div>
    <div class = "mainDiv">
      <div v-on:click = "test" class = "innerDiv">
        <p>2018 / 12 / 13 <B>김술현</B>님의 생일을 축하합니다!</p>
        <img src="../../build/DSC_0048.png"/>
      </div>
    </div>
  </div>
</template>
<script>
import Vue from 'vue'
import axios from 'axios'
import XLSX from 'xlsx'

export default {
  name: 'main',
  async data () {
    let url = "http://localhost:3000/aa"
    let result = await axios.post(url, {data : "some"})
    result = result.data
    var list = []
    for(var i=0;result[i]!=null;i++) list.push(result[i].link)
    return {
      images: list,
      number: 0
    }
  },
  mounted () {
  },
  methods: {
    test () {
      console.log(this.number)
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body{
  margin : 0;
}
.mainDiv {
  background-color: #677e52;
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  -webkit-justify-content: center;
  -webkit-align-items: flex-start;
}
.innerDiv {
  position: relative;
}
img {
  top: 20vh;
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
  width: 60vw;
  height: 70vh;
  background-repeat: no-repeat;
  background-size: contain;
  border-radius: 5em;
}
p {
  font-size: 6vh;
  color: #b7ca79;
}
</style>
