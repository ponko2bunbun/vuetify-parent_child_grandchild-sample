<template>
    <v-textarea
        label="Grandchild"
        v-model="grandchildFieldComputed"
    />
</template>

<script>
export default {
    props: {
        grandchildField: {
            type: String,
            default: null
        }
    },
    computed: {
        grandchildFieldComputed: {
            get () {
                return this.grandchildField
            },
            set (value) {
                this.$emit('update:grandchild-field', value)
            }
        }
    }
}
</script>
