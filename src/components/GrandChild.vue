<template>
    <v-textarea
        label="Grandchild"
        v-model="grandchildFirldComputed"
    />
</template>

<script>
export default {
    props: {
        grandchildFirld: null
    },
    computed: {
        grandchildFirldComputed: {
            get () {
                return this.grandchildFirld
            },
            set (value) {
                this.$emit('update:grandchildFirld', value)
            }
        }
    }
}
</script>
