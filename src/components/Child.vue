<template>
    <v-container>
        <v-row>
            <v-textarea
                label="Child"
                v-model="childFirldComputed"
            />
        </v-row>

        <v-row>
            <GrandChild
                v-bind:grandchild-firld.sync="childFirldComputed"
            />
        </v-row>
    </v-container>
</template>

<script>
import GrandChild from './GrandChild'

export default {
    components: {
        GrandChild
    },
    props: {
        childFirld: null
    },
    computed: {
        childFirldComputed: {
            get () {
                return this.childFirld
            },
            set (value) {
                this.$emit('update:childFirld', value)
            }
        }
    }
}
</script>
