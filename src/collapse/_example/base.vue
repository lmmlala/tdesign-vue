<template>
  <div class="tdesign-collapse">
    <t-collapse :default-value="[1]" @change="handlePanelChange">
      <t-collapse-panel header="这是一个折叠标题">
        这部分是每个折叠面板折叠或展开的内容，可根据不同业务或用户的使用诉求，进行自定义填充。可以是纯文本、图文、子列表等内容形式。
      </t-collapse-panel>
      <t-collapse-panel destroy-on-collapse header="设置默认展开项">
        这部分是每个折叠面板折叠或展开的内容，可根据不同业务或用户的使用诉求，进行自定义填充。可以是纯文本、图文、子列表等内容形式。
      </t-collapse-panel>
      <t-collapse-panel header="自定义折叠面板内容">
        <div class="tdesign-demo-block-column" style="width: 80%">
          <t-tag-input v-model="tags1" clearable />

          <t-tag-input :value="tags2" label="Controlled: " clearable />

          <t-tag-input :default-value="tags3" label="UnControlled: " clearable />
        </div>
      </t-collapse-panel>
      <t-collapse-panel header="嵌套折叠面板">
        <t-collapse default-expand-all>
          <t-collapse-panel header="子面板1"> 这是子面板1 </t-collapse-panel>
          <t-collapse-panel header="子面板2"> 这是子面板2 </t-collapse-panel>
          <t-collapse-panel header="子面板3"> 这是子面板3 </t-collapse-panel>
          <t-collapse-panel header="子面板4"> 这是子面板4 </t-collapse-panel>
        </t-collapse>
      </t-collapse-panel>
    </t-collapse>
    <div style="margin-top: 10px">当前展开项:{{ currentItem }}</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      currentItem: [1],
      tags1: ['Vue', 'React'],
      tags2: ['Vue', 'React'],
      tags3: ['Vue', 'React'],
    };
  },
  methods: {
    handlePanelChange(val) {
      this.currentItem = val;
    },
  },
};
</script>
<style lang="less">
.accordion-demo {
  background-color: #f9f9f9;
}
.button-area {
  margin-top: 20px;
  display: flex;
  align-items: center;
}
</style>
