<script setup>
    import RouterLink from '../components/UI/RouterLink.vue';
    import Heading from '../components/UI/Heading.vue';
    import {FormKit} from '@formkit/vue'

    defineProps({
        titulo: {
            type: String,
            required: true
        }
    })
</script>

<template>
    <div>
        <div class=" flex justify-end">
            <RouterLink to="inicio">
                Volver
            </RouterLink>
        </div>
        <Heading>{{ titulo }}</Heading>

        <div class="mx-10 mt-10 bg-white shadow rounded">
            <div class="mx-auto md:w-1/2 py-10 px-6">
                <FormKit 
                    type="form"
                >
                <FormKit 
                type="text"
                label="Nombre"
                placeholder="Nombre del cliente"
                help="Coloca el nombre del usuario de ingreso"
                validation="required"
                :validation-messages="{required : 'El nombre del cliente es obligatorio'}"
                validation-visibility="live"
                />
                </FormKit>
            </div>
        </div>

    </div>
</template>

<style>
    .formkit-wrapper{
        max-width: 100%;
    }
</style>