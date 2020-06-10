<template>
    <v-textarea
        label="Grandchild"
        v-model="grandchildFieldComputed"
    />
</template>

<script>
export default {
    props: {
        grandchildField: null
    },
    computed: {
        grandchildFieldComputed: {
            get () {
                return this.grandchildField
            },
            set (value) {
                this.$emit('update:grandchildField', value)
            }
        }
    }
}
</script>
