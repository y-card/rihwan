<script setup lang="ts">
import img from "../assets/image/main.png";

const props = defineProps({
  type: String,
});
</script>

<template>
  <div :class="['main_visual', props.type, 'fade-in']">
    <img :src="img" class="main" />
    <p class="main_title">1st birthday</p>
    <p class="main_name">김리환</p>
    <p class="description">첫 생일파티에 초대합니다</p>
    <p class="footer">2025년 1월 18일 오후 6시<br/>아바니 센트럴 호텔 4층 더큐브</p>
  </div>
</template>

<style scoped>
.main_visual {
  position: relative;
  font-family: "Nanum Myeongjo", serif;
  text-align: center;
  min-height: 500px;
}

.main_visual .main {
  width: auto;
  min-height: 500px;
  max-height: 813px;
  transform: translateX(-50%);
  margin-left: 50%;
}

.main_visual .main_title,
.main_visual .main_name,
.main_visual .description,
.main_visual .footer {
  position: absolute;
  left: 0;
  right: 0;
  top: 20px;
  margin: 0 auto;
  color: #beb9a1;
  text-align: center;
  font-size: 17px;
  font-weight: bolder;
  line-height: 50px;
}
.main_visual .main_name {
  position: absolute;
  top: 78px;
  font-size: 50px;
  letter-spacing: 1px;
  color: #333;
  opacity: 0.9;
  line-height: 60px;
}

.main_visual .description {
  top: 133px;
  color: #333;
  opacity: 0.7;
  font-size: 22px;
}

.main_visual .footer {
  bottom: 50px;
  top: unset;
  line-height: normal;
  font-size: 13px;
  color: #333;
  opacity: 0.7;
}

.subtitle {
  margin-bottom: 20px;
  font-size: 20px;
}

.bottom {
  position: absolute;
  bottom: 30px;
  font-size: 20px;
  width: 100%;
}

@media (min-width: var(--breakpoint)) {
}
</style>
