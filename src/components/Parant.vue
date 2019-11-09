<template>
    <v-container>
        <v-row>
            <v-textarea
                label="Parent"
                v-model="firldComputed"
            />
        </v-row>

        <v-row>
            <Child
                v-bind:child-firld.sync="firldComputed"
            />
        </v-row>
    </v-container>
</template>

<script>
import Child from './Child'

export default {
    components: {
        Child
    },
    data: () => ({
        firld: null
    }),
    computed: {
        firldComputed: {
            get () {
                return this.firld
            },
            set (value) {
                this.firld =value
            }
        }
    }
}
</script>
