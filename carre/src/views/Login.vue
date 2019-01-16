<template>
    <v-container fluid>
        <v-responsive>
                <v-container fill-height>
                    <v-layout align-center>
                        <v-flex sm12>
                            <h3 class="display-3">Welcome to the site</h3>

                            <span class="subheading">Lorem ipsum dolor sit amet, pri veniam forensibus id. Vis maluisset molestiae id, ad semper lobortis cum. At impetus detraxit incorrupte usu, repudiare assueverit ex eum, ne nam essent vocent admodum.</span>

                            <v-divider class="my-3"></v-divider>

                            <div class="title mb-3">Check out our newest features!</div>

                            <v-btn
                                    class="mx-0"
                                    color="primary"
                                    large
                            >
                                See more
                            </v-btn>
                        </v-flex>
                        <v-flex sm12>
                            <v-hover>
                                <v-card
                                        slot-scope="{ hover }"
                                        :class="`elevation-${hover ? 12 : 2}`"
                                        class="mx-auto"
                                        width="344"
                                >
                                    <v-card-title class="headline font-weight-regular blue-grey white--text">Profile</v-card-title>
                                    <v-card-text>
                                        <v-subheader class="pa-0">Where do you live?</v-subheader>
                                        <v-autocomplete
                                                v-model="model"
                                                :hint="!isEditing ? 'Click the icon to edit' : 'Click the icon to save'"
                                                :items="states"
                                                :readonly="!isEditing"
                                                :label="`State — ${isEditing ? 'Editable' : 'Readonly'}`"
                                                persistent-hint
                                                prepend-icon="mdi-city"
                                        >
                                            <v-slide-x-reverse-transition
                                                    slot="append-outer"
                                                    mode="out-in"
                                            >
                                                <v-icon
                                                        :color="isEditing ? 'success' : 'info'"
                                                        :key="`icon-${isEditing}`"
                                                        @click="isEditing = !isEditing"
                                                        v-text="isEditing ? 'mdi-check-outline' : 'mdi-circle-edit-outline'"
                                                ></v-icon>
                                            </v-slide-x-reverse-transition>
                                        </v-autocomplete>
                                        <v-autocomplete
                                                v-model="model"
                                                :hint="!isEditing ? 'Click the icon to edit' : 'Click the icon to save'"
                                                :items="states"
                                                :readonly="!isEditing"
                                                :label="`State — ${isEditing ? 'Editable' : 'Readonly'}`"
                                                persistent-hint
                                                prepend-icon="mdi-city"
                                        >
                                            <v-slide-x-reverse-transition
                                                    slot="append-outer"
                                                    mode="out-in"
                                            >
                                                <v-icon
                                                        :color="isEditing ? 'success' : 'info'"
                                                        :key="`icon-${isEditing}`"
                                                        @click="isEditing = !isEditing"
                                                        v-text="isEditing ? 'mdi-check-outline' : 'mdi-circle-edit-outline'"
                                                ></v-icon>
                                            </v-slide-x-reverse-transition>
                                        </v-autocomplete>
                                        <v-autocomplete
                                                v-model="model"
                                                :hint="!isEditing ? 'Click the icon to edit' : 'Click the icon to save'"
                                                :items="states"
                                                :readonly="!isEditing"
                                                :label="`State — ${isEditing ? 'Editable' : 'Readonly'}`"
                                                persistent-hint
                                                prepend-icon="mdi-city"
                                        >
                                            <v-slide-x-reverse-transition
                                                    slot="append-outer"
                                                    mode="out-in"
                                            >
                                                <v-icon
                                                        :color="isEditing ? 'success' : 'info'"
                                                        :key="`icon-${isEditing}`"
                                                        @click="isEditing = !isEditing"
                                                        v-text="isEditing ? 'mdi-check-outline' : 'mdi-circle-edit-outline'"
                                                ></v-icon>
                                            </v-slide-x-reverse-transition>
                                        </v-autocomplete>
                                    </v-card-text>
                                </v-card>
                            </v-hover>
                        </v-flex>
                    </v-layout>
                </v-container>
            </v-responsive>

    </v-container>

</template>

<script>
    export default {
        name: "Login",
        data () {
            return {
                isEditing: false,
                model: null,
                states: [
                    'Alabama', 'Alaska', 'American Samoa', 'Arizona',
                    'Arkansas', 'California', 'Colorado', 'Connecticut',
                    'Delaware', 'District of Columbia', 'Federated States of Micronesia',
                    'Florida', 'Georgia', 'Guam', 'Hawaii', 'Idaho',
                    'Illinois', 'Indiana', 'Iowa', 'Kansas', 'Kentucky',
                    'Louisiana', 'Maine', 'Marshall Islands', 'Maryland',
                    'Massachusetts', 'Michigan', 'Minnesota', 'Mississippi',
                    'Missouri', 'Montana', 'Nebraska', 'Nevada',
                    'New Hampshire', 'New Jersey', 'New Mexico', 'New York',
                    'North Carolina', 'North Dakota', 'Northern Mariana Islands', 'Ohio',
                    'Oklahoma', 'Oregon', 'Palau', 'Pennsylvania', 'Puerto Rico',
                    'Rhode Island', 'South Carolina', 'South Dakota', 'Tennessee',
                    'Texas', 'Utah', 'Vermont', 'Virgin Island', 'Virginia',
                    'Washington', 'West Virginia', 'Wisconsin', 'Wyoming'
                ]
            }
        }
    }
</script>

<style scoped>

</style>