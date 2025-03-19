<script setup>
    defineProps({
        propiedad: {
            typpe: Object
        },
        price: {
            type: Function
        }
    })
</script>

<template>
    <v-col cols="12" md="4">
        <v-card>
            <v-card-title>
                {{ propiedad.titulo }}
            </v-card-title>

            <v-card-text>
                {{ propiedad.descripcion }}
            </v-card-text>

            <v-card-text class="text-h5 font-weight-bold">
                Precio: {{ price(propiedad.precio) }}
            </v-card-text>

            <template v-slot:actions>
                <v-btn block color="info" variant="flat" :to="{name: 'propiedad', params: {id: propiedad.id}}">
                    Ver Información
                </v-btn>
            </template>
        </v-card>
    </v-col>
</template>