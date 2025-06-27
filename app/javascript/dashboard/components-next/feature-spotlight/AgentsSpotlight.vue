<script setup>
import { computed } from 'vue';
import FeatureSpotlight from './FeatureSpotlight.vue';
import { useI18n } from 'vue-i18n';

const props = defineProps({
  showSpotlight: {
    type: Boolean,
    default: true,
  },
  title: {
    type: String,
    default: '',
  },
  note: {
    type: String,
    default: '',
  },
  learnMoreUrl: {
    type: String,
    default:
      'https://www.chatwoot.com/hc/user-guide/articles/683229-agent-management',
  },
});

const { t } = useI18n();

const spotlightTitle = computed(
  () => props.title || t('FEATURE_SPOTLIGHT.AGENTS_MANAGEMENT.TITLE')
);

const spotlightNote = computed(
  () => props.note || t('FEATURE_SPOTLIGHT.AGENTS_MANAGEMENT.DESCRIPTION')
);
</script>

<template>
  <div v-if="showSpotlight" class="mb-6">
    <FeatureSpotlight
      :title="spotlightTitle"
      :note="spotlightNote"
      video-url=""
      thumbnail=""
      fallback-thumbnail="/assets/images/dashboard/agents/team-light.svg"
      fallback-thumbnail-dark="/assets/images/dashboard/agents/team-dark.svg"
      :learn-more-url="learnMoreUrl"
    />
  </div>
</template>
