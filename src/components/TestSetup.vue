<template>
    <ButtonComp class="set-default-button" :mode="mode" :text="buttonText" @click="emit('setDefault')" />
</template>

<script setup>
import { computed } from 'vue';
import i18n from '@/stores/i18n.js';

const { pgettext } = i18n();

const buttonText = computed(() => pgettext('The button for applying default settings.', 'Reset by default'));

defineProps({
    mode: {
        type: String,
        default: 'base',
    },
});

const emit = defineEmits({
    setDefault: null,
});
</script>

<style lang="scss">
.set-default-button {
    margin-bottom: 1px;
}
</style>