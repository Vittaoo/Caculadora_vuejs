<script setup>

    const props = defineProps(['resultado', 'num1', 'num2'])
</script>

<template>
    <div class="d-flex justify-content-center mt-5 fs-1">

        <span class="text-light" v-if="props.num1 && props.num2 != ''">Resultado: {{ props.resultado }}</span>
        <span class="text-light" v-else-if="props.num1 || props.num2 === ''">Digite os números...</span>
    </div>

</template>