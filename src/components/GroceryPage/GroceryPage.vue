<template>
    <v-container style="height: 100vh; background-color: blue">
        <v-row no-gutters style="margin-top: 50px">

            <!-- Search box -->
            <v-col cols="4">
                <v-sheet class="pa-2 ma-2" style="background-color: red;">
                    <v-card class="mx-auto" color="grey-lighten-3" max-width="400">
                        <v-card-text>
                            <v-text-field :loading="loading" density="compact" variant="solo" label="Search templates"
                                append-inner-icon="mdi-magnify" single-line hide-details
                                @click:append-inner="onClick"></v-text-field>
                        </v-card-text>
                    </v-card>
                </v-sheet>
                <template>
                    <v-card class="mx-auto" max-width="300">

                        <v-list :items="items"></v-list>
                    </v-card>
                </template>
            </v-col>

            <!-- Main list of ingredients -->
            <v-col cols="8">
                <v-sheet class="pa-2 ma-2"> .v-col-auto </v-sheet>
            </v-col>

            <!-- Sub list of ingredients -->
            <v-col cols="4">
                <v-sheet class="pa-2 ma-2" style="background-color: red;">
                    <v-card class="mx-auto" max-width="300">
                        <v-list :items="items">
                        </v-list>
                    </v-card>
                </v-sheet>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        items: [
            { type: 'subheader', title: 'Pantry' },
            {
                title: 'Item #1',
                value: 1,
            },
            {
                title: 'Item #2',
                value: 2,
            },
            {
                title: 'Item #3',
                value: 3,
            },
            { type: 'divider' },
            { type: 'subheader', title: 'Group #2' },
            {
                title: 'Item #4',
                value: 4,
            },
            {
                title: 'Item #5',
                value: 5,
            },
            {
                title: 'Item #6',
                value: 6,
            },
        ],
    }),
}
</script>

<style></style>
