<script>
export default {
    name: 'FilterSelect',
    data: () => ({
    
        selectedOption: ''
    }),

    props: {
        defaultValue: String,
        defaultLabel: String,
        options: Array
    },

    emits: ['option-change']
}

</script>

<template>
    <select v-model="selectedOption" @change="$emit('option-change', selectedOption)">
        <option :value="defaultValue || ''">{{ defaultLabel || '---' }}</option>
        <option v-for="(option, i) in options" :key="option.id" :value="option.value">{{ option.label }}</option>
    </select>
</template>
