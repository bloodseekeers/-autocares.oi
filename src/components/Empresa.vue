<template>
    <v-container id="empresa" >
        <h2 class="font-weight:bold;">Empresa</h2>    
        <v-row>
            <v-col class="col-6 d-block pa-2">
            <div class="imagem">
                <v-img
                 class="float-none"
                 src="https://cdn.pixabay.com/photo/2015/01/08/18/27/startup-593336_960_720.jpg"></v-img>
            </div>
            </v-col>
            <v-col class="col-6 d-block pa-2">
                <p>Somos una empresa con más de 25 años de experiencia y que a largo de toda nuestra historia hemos sabido mantenernos fieles a nuestros principios básicos, el trato personalizado de cada uno de nuestros clientes, la constante renovación de nuestra flota con la máxima seguridad, confort, calidad y las ultimas y más modernas innovaciones de nuestros vehículos.</p>
                 <P>Disponemos de un equipo humano muy profesional y con dilatada experiencia que estarán siempre dispuestos a ayudarles y asesorarles, ofreciéndole los mejores servicios de transporte con unos precios muy competitivos.</P>
            </v-col>
        </v-row>
        
    </v-container>   

</template>
<script>
export default {
    name: 'Empresa',
}
</script>
<style>
#servicios{
    font-size: 25x;
}
h2{
    font-size: 40px;
}

</style>