<template>
    <ButtonComp class="set-default-button" :type="type" :mode="mode" :disabled="disabled" :text="buttonText"
        @click="emit('setDefault')" />
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
    type: {
        type: String,
        default: 'text',
    },
    disabled: {
        type: Boolean,
        default: false,
    },
});
const emit = defineEmits({
    setDefault: null,
});
</script>

<style lang="scss"></style>