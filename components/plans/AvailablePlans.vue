<script setup lang="ts">
const { t } = useI18n();
const css = useCssModule();
</script>

<template>
  <div :class="css.wrapper">
    <div>
      <div :class="css.header">{{ t('home.plans.title') }}</div>
    </div>
    <div :class="css.basic">
      <div :class="css.content">
        <FreePlan />
        <BasicPlan />
        <AdvancedPlan v-if="false" />
      </div>
    </div>
    <CustomPlan v-if="false" />
  </div>
</template>

<style lang="scss" module>
@import '@/assets/css/main.scss';
@import '@/assets/css/media.scss';

.wrapper {
  padding: 7.5rem 0;
}

.header {
  @apply font-bold text-rui-text;

  text-align: center;
  letter-spacing: -0.03em;
  padding-right: $mobile-margin;
  padding-left: $mobile-margin;

  @include text-size(84px, 108px);
}

.basic {
  @apply container;
}

.content {
  @apply flex-wrap flex-row flex lg:justify-around justify-center;
}
</style>
