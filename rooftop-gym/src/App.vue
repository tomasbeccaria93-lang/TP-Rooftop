<script>
import Contacto from './componentes/Contacto.vue';
import Encabezado from './componentes/Encabezado.vue';
import Footer from './componentes/Footer.vue';
import Inicio from './componentes/Inicio.vue';
import Servicios from './componentes/Servicios.vue';

export default {
    components: {
        Encabezado, Inicio, Servicios, Contacto, Footer}
}
</script>

<template>
<Encabezado />
<Inicio />
<Servicios />
<Contacto />
<Footer />

</template>

<style scoped></style>
