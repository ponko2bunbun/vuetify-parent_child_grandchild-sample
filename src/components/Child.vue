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
                v-model:grandchild-field="childFieldComputed"
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
        childField: {
            type: String,
            default: null
        }
    },
    computed: {
        childFieldComputed: {
            get () {
                return this.childField
            },
            set (value) {
                this.$emit('update:child-field', value)
            }
        }
    }
}
</script>
