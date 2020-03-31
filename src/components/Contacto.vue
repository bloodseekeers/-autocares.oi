<template>
    <v-container id="contacto" >
        <v-card data-aos="zoom-in-down" data-aos-duration="1500">            
        <v-row>
            <v-col class="formul col-sm-8 col-md-4 col-xl-6 mt-xl-4">
                <h2 class="ml-2 text-sm-center">Contacto</h2>
                <v-form>
                    <v-text-field class="ml-5"
                    v-model="name"
                    :error-messages="nameErrors"
                    label="Nombre"
                    required
                    @input="$v.name.$touch()"
                    @blur="$v.name.$touch()"
                    ></v-text-field>
                    <v-text-field class="ml-5"
                    :error-messages="emailErrors"
                    @input="$v.name.$touch()"
                    @blur="$v.name.$touch()"
                    v-model="email"
                    label="Email"
                    required
                    ></v-text-field>
                    <v-text-field
                    class="ml-5"
                    v-model="telf"
                    :error-messages="telfErrors"
                    @input="$v.name.$touch()"
                    @blur="$v.name.$touch()"
                    label="Telf"
                    required
                    type="number"
                    :counter="12"
                    ></v-text-field>
                    <v-textarea
                    class="ml-5"
                    label="Mensaje"
                    required
                    :error-messages="messengerErrors"
                    @input="$v.name.$touch()"
                    @blur="$v.name.$touch()"
                    v-model="messenger"
                    ></v-textarea>
                    <div class="text-center">
                    <v-btn
                    class="white--text"
                    color="#1c8b25"
                    @click="submit">Enviar</v-btn>
                    </div>
                </v-form>
            </v-col>
             <v-col class="col-md-5 ml-md-12 col-xl-4 mt-xl-4  col-lg-5 imga">
                  <v-img
                class="mt-0 mb-5 ml-5 mr-4"
                max-width="800px"
                max-height="600px"
                src="../assets/contacto.jpg"
            ></v-img>
            </v-col>
            <v-row>
                <v-col class="col-7 inf ml-9 col-xs-12 col-lg-6 col-xl-7">
                    <h4 class="ml-6">Dirección</h4>
                    <p class="ml-6">C/ Fray Bartolomé de las Casas, 63 El Viso del Alcor, Sevilla <br/> Telf: <a href="tel:+34692202752">692202752</a> <br/>Email: <a href="mailto:example@example.com">example@example-com</a></p>
                </v-col>
                <v-col class="col-4 ml-0 col-xs-0" > 
                    <div class="map-responsive"><iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3169.77845918789!2d-5.721734584693258!3d37.39507117983041!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xd1289e7e2208c67%3A0xafcb354736e3fde8!2sCalle%20Fray%20Bartolom%C3%A9%20de%20las%20Casas%2C%2063%2C%2041520%20El%20Viso%20del%20Alcor%2C%20Sevilla!5e0!3m2!1ses!2ses!4v1585528385299!5m2!1ses!2ses" width="490" height="160" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe></div>
                </v-col>
            </v-row>
            <v-row class="d-flex d-sm-none">
                <div class="ml-12"><iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3169.77845918789!2d-5.721734584693258!3d37.39507117983041!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xd1289e7e2208c67%3A0xafcb354736e3fde8!2sCalle%20Fray%20Bartolom%C3%A9%20de%20las%20Casas%2C%2063%2C%2041520%20El%20Viso%20del%20Alcor%2C%20Sevilla!5e0!3m2!1ses!2ses!4v1585528385299!5m2!1ses!2ses" width="250" height="160" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe></div>
            </v-row>

        </v-row>
        </v-card>
    </v-container>
</template>
<script>
  import { validationMixin } from 'vuelidate'
  import { required, maxLength, email } from 'vuelidate/lib/validators'
export default {
     mixins: [validationMixin],
    validations: {
      name: { required },
      email: {required, email },
      telf: {required, maxLength: maxLength(12) },
      messenger:{required}
    },
    data: () => ({
        name: '',
        email: '',
        telf: '',
        messenger: '',
    }),
    computed:{
       emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('El correo electronico debe ser valido')
        !this.$v.email.required && errors.push('E-mail es necesario')
        return errors
      },
        nameErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.required && errors.push('El nombre es necesario')
        return errors
      },
      messengerErrors () {
          const errors = []
          if (!this.$v.messenger.$dirty) return errors
          !this.$v.messenger.required && errors.push('El mensaje es necesario')
          return errors
      },
      telfErrors(){
          const errors = []
          if (!this.$v.telf.$dirty) return errors
          !this.$v.telf.required && errors.push('El numero de telf es necesario')
          !this.$v.telf.maxLength && errors.push('El numero de telf debe tener como maximo 12 numeros')
          return errors
      },
    },
    methods: {
        submit () {
            this.$v.$touch()
        },
    },
}
</script>
<style>
.map-responsive{
    overflow:hidden;
    padding-bottom:56.25%;
    position:relative;
    height:0;
}
.map-responsive iframe{
    left:0;
    top:0;
    height:100%;
    width:100%;
    position:absolute;
}
.inf p a{
    color: green;
}
.cardtitle{
    margin-right: auto;
    margin-left: 32em;
    margin-bottom: 3em;
}
.formul{
    margin-left: 8em;
    margin-right: 2em;
}

@media only screen and (max-width: 958px){

    .imga{
        display: none;
    }
}
@media only screen and (max-width: 600px) {
 .formul{
     margin-left: auto;
 }
.map-responsive{
    display: none;
}
}
</style>