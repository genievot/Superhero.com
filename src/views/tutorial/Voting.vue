<template>
  <div class="tutorial-page">
    <h1>{{ $t('views.Voting.header') }}</h1>
    <hr width="30%">

    <i18n
      v-for="(item, index) in $t('views.Voting.sections').length"
      :key="index"
      :path="`views.Voting.sections[${index}].text`"
      tag="p"
    />
  </div>
</template>

<script>
export default {
  metaInfo: {
    title: 'Tutorial Voting Page',
  },
};
</script>
