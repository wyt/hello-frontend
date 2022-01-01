<template>
  <div
    class="w-comb"
    :style="{
      width: initWidth + 'px',
      height: initHeight + 'px',
      marginRight: spacing * 2 + 'px',
      backgroundColor: color
    }"
  >
    <!-- 文本内容start -->
    <div class="w-comb-content">{{ value }}</div>
    <!-- 文本内容end -->
    <div class="w-comb-sub1" :style="{ backgroundColor: color }"></div>
    <div class="w-comb-sub2" :style="{ backgroundColor: color }"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    RADICAL_3: {
      type: Number,
      default: 1.7320508
    },
    // 设置蜂巢大小
    size: Number,
    // 间距
    spacing: {
      type: Number,
      default: 3
    },
    // 设置蜂巢背景色
    color: {
      type: String,
      default: "#e4e4e4"
    },
    // 蜂巢内文本
    value: String
  },
  computed: {
    initWidth() {
      return this.size || 80;
    },
    initHeight() {
      return Math.ceil(this.initWidth / this.RADICAL_3);
    }
  }
};
</script>

<style scoped>
.w-comb {
  display: inline-block;
  position: relative;
  cursor: pointer;
}

.w-comb-content {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 100;
  display: flex;
  font-size: 13px;
	color: #fff;
  align-items: center;
  justify-content: center;
  background: transparent;
}
.w-comb-sub1,
.w-comb-sub2 {
  position: absolute;
  width: inherit;
  height: inherit;
}

.w-comb-sub1 {
  transform: rotate(-60deg);
}

.w-comb-sub2 {
  transform: rotate(60deg);
}
</style>
