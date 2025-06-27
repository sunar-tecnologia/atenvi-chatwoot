<script setup>
import AgentsSpotlight from './AgentsSpotlight.vue';
</script>

<template>
  <Story
    title="Components/FeatureSpotlight/AgentsSpotlight"
    :layout="{ type: 'grid', width: '1000px' }"
  >
    <Variant title="Agents Management Spotlight">
      <div class="p-6 bg-n-background">
        <AgentsSpotlight />
      </div>
    </Variant>

    <Variant title="With Custom Content">
      <div class="p-6 bg-n-background">
        <AgentsSpotlight
          title="Gestão Avançada de Agentes"
          note="Uma gestão eficiente de agentes é fundamental para o sucesso do seu atendimento. Distribua conversas de forma inteligente, monitore performance, defina permissões específicas e mantenha sua equipe sempre produtiva e engajada."
          learn-more-url="https://www.chatwoot.com/hc/user-guide/articles/683229-agent-management"
        />
      </div>
    </Variant>
  </Story>
</template>
