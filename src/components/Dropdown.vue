<template>
  <div class="aggregator__dropdown">
    <b-form-select
      v-model="selectedVal"
      :options="optionsVal"
      @change="method(selectedVal)"
    />
  </div>
</template>

<script>
export default {
  name: 'VueDropdown',
  props: {
    options: { type: Array, default: null },
    selected: { type: String, default: '' },
    method: { type: Function, required: true },
  },
  data() {
    return {
      selectedVal: this.selected,
      optionsVal: this.options,
    };
  },
};
</script>

<style lang="scss" scoped>
.aggregator__dropdown{
  display: inline-block;
  margin: unset;
  select{
    background: none;
    background-color: $background_color;
    color: $primary_color;
    font-size: .75rem;
    border: none;
    &:focus{
      color: $primary_color;
    }
  }
}
</style>