<template>
  <div class="tdesign-demo-block demo-card">
    <t-card :title="title" :bordered="false" hover-shadow :style="{ width: '400px' }">
      {{ infoMessage }}
      <template #actions>
        <a href="javascript:void(0)" @click="clickHandler">操作</a>
      </template>
    </t-card>
  </div>
</template>
<script>
import { MessagePlugin } from 'tdesign-vue';

export default {
  data() {
    return {
      title: '标题',
      actions: '操作',
      infoMessage:
        '仅有内容区域的卡片形式。卡片内容区域可以是文字、图片、表单、表格等形式信息内容。可使用大中小不同的卡片尺寸，按业务需求进行呈现。',
    };
  },
  methods: {
    clickHandler() {
      MessagePlugin.success('操作');
    },
  },
};
</script>
<style lang="less" scoped>
.demo-card {
  padding: 16px;
  background-color: var(--td-bg-color-container-hover);
}
.demo-card /deep/ .t-card__actions {
  line-height: 24px;
}
</style>
