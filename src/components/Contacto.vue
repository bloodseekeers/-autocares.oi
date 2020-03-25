<template>
    <v-container>
        <v-card>
            <div class="cardtitle">
                <v-card-title>Contacto</v-card-title>
            </div>            
        <v-row>
            <v-col class="formul">
                <v-form>
                    <v-text-field class="ml-5"
                    v-model="name"
                    :rules="nameRules"
                    label="Name"
                    required
                    ></v-text-field>
                    <v-text-field class="ml-5"
                    v-model="email"
                    :rules="emailRules"
                    label="Email"
                    required
                    ></v-text-field>
                    <v-text-field
                    class="ml-5"
                    v-model="telf"
                    :rules="tefRules"
                    label="Telf"
                    required
                    type="number"
                    :counter="12"
                    ></v-text-field>
                    <v-textarea
                    class="ml-5"
                    label="Mensaje"
                    required
                    :rules="messengerRules"
                    v-model="mensaje"
                    ></v-textarea>
                    <div class="text-center">
                    <v-btn
                    color="success"
                    @click="submit"
                    >Enviar</v-btn>
                    </div>
                </v-form>
                <v-row class="mt-5" >
                    <v-col class="col-6">
                    <p>
                     <span> C/fray Bartolome de las casas, 63</span>
                     <br><span>41520 El Viso del Alcor, Sevilla</span>
                     <br>Telf:  <a href="tel:+34692202752">692202752</a>
                     <br>Email: <a href="mailto:example@hotmail.com">example@hotmail.com</a>
                    </p>
                    </v-col>
                    <v-col class="col-6">
                        <div style="width: 100%"><iframe width="100%" height="150" src="https://maps.google.com/maps?width=100%&amp;height=300&amp;hl=en&amp;q=Calle%20Fray%20Bartolom%C3%A9%20de%20las%20Casas%2063+(Juan%20Parejo%20Autocares%20S.L)&amp;ie=UTF8&amp;t=&amp;z=18&amp;iwloc=B&amp;output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0"><a href="https://www.maps.ie/coordinates.html">find my coordinates</a></iframe></div><br />
                    </v-col>
                </v-row>
            </v-col>
            <v-col>
                  <v-img
                class="mt-0 mb-5 ml-5 mr-4"
                max-width=""
                src="https://images.unsplash.com/photo-1523966211575-eb4a01e7dd51?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=353&q=80"
            ></v-img>
            </v-col>

        </v-row>
        </v-card>
    </v-container>
</template>
<script>
export default {
    name: 'Contacto',
}
</script>
<style>
.cardtitle{
    margin-right: auto;
    margin-left: 32em;
    margin-bottom: 3em;
}
.formul{
    margin-left: 8em;
    margin-right: 2em;
}
a{
    text-decoration: none;
    color: #000;
}
</style>