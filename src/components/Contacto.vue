<template>
    <v-container id="contacto" >
        <v-card data-aos="zoom-in-down" data-aos-duration="1500">
            <div class="cardtitle">
                <v-card-title>Contacto</v-card-title>
            </div>            
        <v-row>
            <v-col class="formul">
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
                    color="success"
                    @click="submit"
                    >Enviar</v-btn>
                    </div>
                </v-form>
                <v-row class="mt-5" >
                    <v-col class="col-5 mr-1">
                    <p>
                     <span> C/Fray Bartolome de las casas, 63</span>
                     <br><span>41520 El Viso del Alcor, Sevilla</span>
                     <br>Telf:  <a href="tel:+34692202752">692202752</a>
                     <br>Email: <a href="mailto:example@hotmail.com">example@hotmail.com</a>
                    </p>
                    </v-col>
                    <v-col class="col-4 ml-5">
                        <div style="width: 100%"><iframe width="200%" height="200" src="https://maps.google.com/maps?width=100%&amp;height=300&amp;hl=en&amp;q=Calle%20Fray%20Bartolom%C3%A9%20de%20las%20Casas%2063+(Juan%20Parejo%20Autocares%20S.L)&amp;ie=UTF8&amp;t=&amp;z=18&amp;iwloc=B&amp;output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0"><a href="https://www.maps.ie/coordinates.html">find my coordinates</a></iframe></div><br />
                    </v-col>
                </v-row>
            </v-col>
            <v-col>
                  <v-img
                class="mt-0 mb-5 ml-5 mr-4"
                max-width="500px"
                src="../assets/contacto.jpg"
            ></v-img>
            </v-col>

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