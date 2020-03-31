<template>
    <v-container id="servicios">
        <v-card data-aos="flip-left" data-aos-duration="1200">
        <v-row>
            <v-col   md="6" xs="5" cols="12">
                <div class="imagem mr-8 ml-8 ">
                <v-img
                 min-width=""
                 max-height=""
                 src="../assets/Servicio.jpg"></v-img>
                </div>
            </v-col>
            <v-col cols="12"
            xs="12" md="5" class="ml-3 mr-1">
            <h2 class="text-center">Servicios</h2>
                <h4>Nuestra empresa se adapta a todas las necesidades de los clientes.</h4>
                <p class="text-left ml-0">Juan Parejo Autocares S.L. abarca todos los ámbitos del transporte de personas, ofreciendo nuestros mejores servicios y siempre con una atención personalizada en:</p>
                <ul>
                    <li>
                        Congresos
                    </li>
                    <li>
                        Convenciones e Incentivos
                    </li>
                    <li>
                        Agencias
                    </li>
                    <li>
                        Touroperadores
                    </li>
                    <li>
                        Colegios
                    </li>
                    <li>
                        Entidades Deportivas Y Culturales
                    </li>
                    <li>
                        Empresas y Organismos Oficiales
                    </li>
                    <li>
                        Particulares
                    </li>
                </ul>
                <h4>Seguridad</h4>
                <p class="text-left ml-0">Nuestros autocares cumplen con toda la normativa actualizada en materia de seguridad tanto activa como pasiva.</p>
                <div class="text-center">
                    <v-btn class="white--text mt-3 mb-3" color="#1c8b25"
                        target="blank"
                        href="https://api.whatsapp.com/send?phone=34637328460"
                    >Pide Presupuesto</v-btn>
                </div>
            </v-col>
        </v-row>
        </v-card>
    </v-container>   

</template>
<script>
export default {
    name: 'Servicios',
}
</script>
<style>
h2{
    font-size: 40px;
}


</style>