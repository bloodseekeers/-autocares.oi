<template>
<v-container id="empresa">
    <v-card data-aos="flip-down" data-aos-duration="1100">
        <div class="text-center">
        <v-card-title>Empresa</v-card-title>
        </div>
        <v-row>
            <v-col  md="6" xs="5" cols="12">
            <div class="imagem ml-8 mr-8 mt-sm-12 mt-xs-0">
                <v-img
                src="https://cdn.pixabay.com/photo/2015/01/08/18/27/startup-593336_960_720.jpg"></v-img>
            </div>
            </v-col>
            <v-col cols="12"
            xs="12" md="5" class="ml-0 mr-1">
                <p>Somos una empresa con más de 25 años de experiencia y que a largo de toda nuestra historia hemos sabido mantenernos fieles a nuestros principios básicos, el trato personalizado de cada uno de nuestros clientes, la constante renovación de nuestra flota con la máxima seguridad, confort, calidad y las ultimas y más modernas innovaciones de nuestros vehículos.</p>
                 <P>Disponemos de un equipo humano muy profesional y con dilatada experiencia que estarán siempre dispuestos a ayudarles y asesorarles, ofreciéndole los mejores servicios de transporte con unos precios muy competitivos.</P>
            </v-col>
        </v-row>
        
    </v-card>   
</v-container>
</template>
<script>
export default {
    name: 'Empresa',
}
</script>
<style>

p{
    text-align:justify;
    margin: 1em;
    text-decoration: none;
}

</style>