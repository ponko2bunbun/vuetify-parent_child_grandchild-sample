<template>
    <v-app>
        <v-main>
            <v-container class="pa-0">
                <v-row>
                    <v-col>
                        <Parant/>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
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
