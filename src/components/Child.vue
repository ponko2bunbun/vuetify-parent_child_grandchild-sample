<template>
    <v-container>
        <v-row>
            <v-textarea
                label="Child"
                v-model="childFieldComputed"
            />
        </v-row>

        <v-row>
            <GrandChild
                v-bind:grandchild-field.sync="childFieldComputed"
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
        childField: null
    },
    computed: {
        childFieldComputed: {
            get () {
                return this.childField
            },
            set (value) {
                this.$emit('update:childField', value)
            }
        }
    }
}
</script>
