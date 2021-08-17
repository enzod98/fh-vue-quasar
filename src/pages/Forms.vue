<template>
  <q-page class="q-ma-md">
    <span class="text-h3">Forms</span>
    <q-separator spaced />
    <div class="row justify-center">
      <div class="col-12 col-sm-8">
        <q-form
          @submit="onSubmit"
          @reset="onReset"
          class="q-gutter-xs q-pt-md"
        >
          <q-input
            filled
            v-model="userForm.email"
            type="email"
            label="Correo electrónico"
            lazy-rules
            :rules="[ 
              val => val && val.length > 0 || 'Este campo es obligatorio',
              isValidEmail
            ]"
          />
          <q-input
            filled
            type="password"
            v-model="userForm.pass1"
            label="Contraseña"
            lazy-rules
            :rules="[ val => val && val.length > 0 || 'Este campo es obligatorio']"
          />

          <q-input
            filled
            type="password"
            v-model="userForm.pass2"
            label="Repetir contraseña"
            lazy-rules
            
            :rules="[ val => val && val.length > 0 || 'Este campo es obligatorio',
                      isSamePassword
            ]"
          />

          <q-checkbox v-model="userForm.conditions" label="Acepto los términos y condiciones" 
            :style=" userForm.errorInConditions && !userForm.conditions && 'color:red' "
          />
          

          <div class="row justify-end">
            <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
            <q-btn label="Submit" type="submit" color="primary"/>
          </div>
        </q-form>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import { useQuasar } from 'quasar'

export default defineComponent({
  name: "Forms",
  setup () {
    const $q = useQuasar()
    $q.iconSet.field.error = "las la-bug";

    const userForm = ref({
      email: '',
      pass1: '',
      pass2: '',
      conditions: false,
      errorInConditions: false
    })
    

    return {
      userForm,
      onSubmit(){
        console.log(userForm.value);
        
        if( !userForm.value.conditions ) userForm.value.errorInConditions = false;

        if( !userForm.value.errorInConditions ){
          userForm.value.errorInConditions = true;
          $q.notify({
            message: 'Debe aceptar los términos y condiciones',
            icon: 'las la-exclamation-circle'
          })
          return
        }
      },
      onReset(){
        userForm.value = {
          email: '',
          pass1: '',
          pass2: '',
          conditions: false,
          errorInConditions: false
        }
      },
      isValidEmail( val ) {
        const emailPattern = /^(?=[a-zA-Z0-9@._%+-]{6,254}$)[a-zA-Z0-9._%+-]{1,64}@(?:[a-zA-Z0-9-]{1,63}\.){1,8}[a-zA-Z]{2,63}$/;
        return emailPattern.test(val) || 'El correo no parece ser válido';
      },
      isSamePassword( val ){
        return ( val === userForm.value.pass1 ) ? true : 'Las contraseñas deben ser iguales'
      }
    }
  }
});
</script>
