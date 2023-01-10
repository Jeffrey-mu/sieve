<script lang="ts" setup>
let count = ref<number>(6)
</script>
<template>
<div b w-100 h-100 ma p-2>

<div :class="'count' + count + ' box'" ma my-10 flex>
  <div v-for="item in count">

  </div>
</div>
  <button v-for="item in 6" btn mx-2 @click="count = item">{{ item }}</button>
  <button @click="count = Math.ceil(Math.random() * 6)" btn my-2>随机</button>
</div>
</template>
<style>
.box {
  background: rgb(233, 229, 229);
  width: 100px;
  height: 100px;
  justify-content: center;
  align-items: center;
  padding: 2px;
  box-sizing: content-box;
  border-radius: 15px;
  box-shadow: -6px 6px 8px inset rgba(255, 255, 255, 0.6),
      6px -6px 8px inset rgba(0, 0, 0, 0.2);
}
.box div {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background-color: black;
  transition: .3s;
}
.count1 {

}
.count1 div {
  width: 40px;
  height: 40px;
  background-color: red;
}
.count2 {
  justify-content: space-around;
}
.count3 {
  align-items: start;
}

.count3 div:nth-child(2){
  margin-top: 30px;
}
.count3 div:nth-child(3) {
  margin-top: 60px;
}
.count4 {
  align-items: start;
  flex-wrap:wrap;
}
.count4 div:nth-child(2n+0) {
  margin-left: 30px;
}
.count4 div {
  margin-top: 10px;
}
.count5 {
  align-items: start;
  flex-wrap: wrap;
}

.count5 div:nth-child(2n+0) {
  margin-left: 30px;
}
.count5 div:nth-child(3) {
  margin: 0 30px;
}
.count5 div:nth-child(4) {
  margin-left: 0px;
}
.count5 div:nth-child(5) {
  margin-left: 30px;
}
.count5 div {
}
.count6 {
  align-items: start;
  flex-wrap: wrap;
}

.count6 div:nth-child(2n+0) {
  margin-left: 30px;
}

.count6 div {
}
</style>
