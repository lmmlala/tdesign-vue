<template>
  <t-space direction="vertical">
    <t-date-range-picker allow-input clearable @pick="onPick" @change="onChange" />
    <t-date-range-picker enable-time-picker allow-input clearable @pick="onPick" @change="onChange" />
  </t-space>
</template>

<script>
export default {
  methods: {
    onPick(value, context) {
      console.log('onPick:', value, context);
    },
    onChange(value) {
      console.log('onChange:', value);
    },
  },
};
</script>
