<template>
    <v-app>
        <v-content>
            <v-container pa-0>
                <v-row>
                    <v-col>
                        <Parant/>
                    </v-col>
                </v-row>
            </v-container>
        </v-content>
    </v-app>
</template>

<script>
import Parant from './components/Parant';

export default {
    name: 'App',

    components: {
        Parant,
    },

    data: () => ({
        //
    }),
};
</script>
