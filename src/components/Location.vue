<script setup lang="ts">
import KakaoMap from "./atom/KakaoMap.vue";
import LocationButton from "./atom/LocationButton.vue";
import LocationText from "./atom/LocationText.vue";
import TextCopy from "./atom/TextCopy.vue";
const props = defineProps({
  type: String,
});
</script>

<template>
  <KakaoMap />
  <TextCopy
    :class="['location_copy', type]"
    copy-text="대전광역시 유성구 동서대로 639"
  >
    <slot>
      <p><em>아바니 센트럴 부산 더큐브</em></p>
      <p>부산 남구 전포대로 133 아바니센트럴부산 4층 더큐브</p>
    </slot>
  </TextCopy>
  <div :class="['btn_locations', type]">
    <LocationButton type="kakao" link="https://kko.kakao.com/Oi5gL5_S1s"
      ><span class="loc_text">카카오네비</span></LocationButton
    >
    <LocationButton type="tmap" link="https://tmap.life/4e41b09c"
      ><span class="loc_text">티맵</span></LocationButton
    >
    <LocationButton type="naver" link="https://naver.me/FsRs4ZfN"
      ><span class="loc_text">네이버지도</span></LocationButton
    >
  </div>
  <div :class="['text_locations', type]">
    <LocationText title="주차안내">
      <p class="text">
        - 아바니 센트럴 호텔 주차장은 주차장 회전교차로 기준 왼쪽편 입니다(판매시설 주차장과 동일)        
      </p>
      <br/>
      <p class="text">★ 오른쪽 오피스텔 주차장은 별개의 시설이며, 주차 등록이 불가하오니 유의하시어 입차 바랍니다.</p>
    </LocationText>
  </div>
</template>

<style>
.btn_locations {
  display: flex;
  gap: 4px;
  margin: 0 auto;
}
.text_locations {
  margin-top: 30px;
}

.location_copy,
.text_locations .text {
  font-family: "NanumSquare", sans-serif;
  font-size: 12px;
}

.location_copy em {
  font-style: normal;
  font-weight: bold;
}

.btn_locations .text {
  font-size: 13px;
}

.location_copy.default,
.btn_locations.default .text,
.text_locations.default .text {
  font-family: "NanumSquare", sans-serif;
  font-size: 12px;
  color: #000;
  font-weight: 400;
}

.text_locations.default .text {
  font-size: 16px;
  font-weight: 400;

}

.loc_text {
  font-size: 11px;
  font-family: "NanumSquare", sans-serif;
  color: #222;
}
</style>
