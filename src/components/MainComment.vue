<script setup lang="ts">
import Divider from "./atom/Divder.vue";

const props = defineProps({
  type: String,
});

let openingComment =
  "깊어져요, 우리,<br/>시간과 함께 낡아지지 말고.<br/>우리의 사랑도 그렇게 될 수 있도록 기억하기로 해요.<br/>오랜 시간을 함께한다는 것의 가치를. 그 힘을.<br /><br />정현주, <그래도 사랑>";
let title = "";
let description =
  "어느덧 1년, 많은 관심과 사랑으로<br/>무럭무럭 자란 리환이가<br/>첫번째 생일을 맞이했습니다.<br/><br/>소중한 자리에 소중한 분들을 모시고자 합니다.<br/><br/>바쁘시더라도 귀한 걸음하시어<br/>리환이의 생일을 축하해주시면 감사하겠습니다.<br/><br/><em class='parents-name'>아빠 김봉현, 엄마 설민비 올림</em>";
</script>

<template>
  <div :class="['main_comment', type]">
    <Divider />
    <!-- <p :class="['poet', 'fade-in']" v-html="openingComment"></p> -->
  </div>
  <div :class="['invitation', type]">
    <div class="fade-in">
      <div class="date">
        <p class="date_comment" v-html="title"></p>
        <p>2025년 1월 18일 오후 6시</p>
        <p>아바니 센트럴 호텔 4층 더큐브</p>
      </div>
      <p class="comment" v-html="description"></p>
    </div>
  
  </div>
</template>

<style scoped>
.main_comment,
.invitation {
  position: relative;
  font-family: "Nanum Myeongjo", serif;
  font-weight: bolder;
  text-align: center;
  line-height: 2rem;
  color: var(--vt-c-black-soft);
  font-weight: 400;
  text-align: center;
  letter-spacing: -0.5px;
  font-size: 18px;
}

.invitation .date {
  color: var(--vt-c-beige-dark);
}

.invitation .date_comment {
  /* font-size: 18px; */
}

.invitation .comment {
  margin: 2rem 0 3rem;
}

.names p {
  font-family: "Nanum Myeongjo", serif;
  color: var(--vt-c-beige-dark);
  font-weight: 500;
  line-height: 25px;
}

.names em {
  font-style: normal;
  font-size: 15px;
  color: var(--vt-c-black-mute);
}

.comment:deep .parents-name{
  font-style: normal;
  font-weight: 700;
}
</style>
