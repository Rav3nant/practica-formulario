<script setup>
  import {reactive} from 'vue'
  import QuickvForm from '@/components/QuickvForm.vue'
  import QuickvInput from '@/components/QuickvInput.vue'

  const formData = reactive({
    firstName:'',
    lastName:'',
    email:'',
    phoneNumber:'',
    age:'',
    password:''
  })
  


</script>
<template>
  <div>
    <quickv-form formId="authForm" name="myAuthForm" class="text-left mb-3 dark:text-blue-700">
      <div class="max-h-[50vh] overflow-auto sm:w-4/12 mx-auto">
        <QuickvInput
          inputId="firstName"
          inputName="myInputFirstName"
          fieldPlaceholder="Nombre" 
          label="Nombre"
          qvRules='required|minlength:3|maxlength:20'
          qvMessages='Campo Obligatorio |   El nombre debe ser de minimo 3 caracteres | El nombre no debe exceder 20 caracteres'
          qvInvalidClass='border border-red-500'
          qvValidClass='border border-green-500'
          v-model="formData.firstName"
        />
        <QuickvInput
          inputId="lastName"
          inputName="myInputLastName"
          fieldPlaceholder="Apellidos" 
          label="Apellidos"
          qvRules='required|minlength:3|maxlength:20'
          qvMessages='Campo Obligatorio |   El apellido debe ser de minimo 3 caracteres | El apellido no debe exceder 20 caracteres'
          qvInvalidClass='border border-red-500'
          qvValidClass='border border-green-500'
          v-model="formData.lastName"
        />
        <QuickvInput
          inputId="email"
          inputName="myInputEmail"
          type="email"
          fieldPlaceholder="E-Mail" 
          label="E-Mail"
          qvRules='required|email'
          qvMessages='Campo Obligatorio | E-Mail Invalido'
          qvInvalidClass='border border-red-500'
          qvValidClass='border border-green-500'
          v-model="formData.email"
        />
        <QuickvInput
          inputId="phoneNumber"
          inputName="myInputPhone"
          type="number"
          fieldPlaceholder="Telefono" 
          label="Telefono"
          qvRules='required|number'
          qvMessages='Campo Obligatorio | Telefono Invalido'
          qvInvalidClass='border border-red-500'
          qvValidClass='border border-green-500'
          v-model="formData.phoneNumber"
        />
        <QuickvInput
          inputId="age"
          inputName="myInputAge"
          type="number"
          fieldPlaceholder="Edad" 
          label="Edad"
          qvRules='required|number|between:18,35'
          qvMessages='Campo Obligatorio | Numero Invalido| La Edad debe ser entre 18 y 35 años'
          qvInvalidClass='border border-red-500'
          qvValidClass='border border-green-500'
          v-model="formData.age"
        />
        <QuickvInput
          inputId="password"
          inputName="myInputPassword"
          type="password"
          fieldPlaceholder="Contraseña" 
          label="Contraseña"
          qvRules='required|password'
          qvMessages='Campo Obligatorio |Contraseña Invalida ,La Contraseña debe contener  !@#$%^&*(),.?":{}|<>'
          qvInvalidClass='border border-red-500'
          qvValidClass='border border-green-500'
          v-model="formData.password"
        />
      </div>


    </quickv-form>

  </div>
</template>

<style  scoped>

</style>