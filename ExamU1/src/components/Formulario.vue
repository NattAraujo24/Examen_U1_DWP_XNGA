<template>
    <b-container>
      <b-row>
        <b-col>
          <b-form @submit="onSubmit" @reset="onReset" v-if="show">
            <!--Marca-->
            <b-form-group id="input-group-marca" label="Marca:" label-for="input-marca">
              <b-row>
                <b-col>
                  <b-form-input id="input-marca" v-model="form.marca" placeholder="marca"
                    required></b-form-input>
                </b-col>
                <!-- Modelo -->
                <b-col>
                  <b-form-input v-model="form.modelo" placeholder="Modelo"
                    required></b-form-input>
                </b-col>
              </b-row>
            </b-form-group>
  
            <!-- año -->
            <b-form-group id="input-group-año" label="Año:" label-for="input-año">
              <b-form-input id="input-año" v-model="form.año" type="date"
                required></b-form-input>
            </b-form-group>
  
            <!-- Numero de serie -->
            <b-form-group id="input-group-numse" label="Numero de serie:"
              label-for="input-numse">
              <b-form-input id="input-numse" v-model="form.numse"  placeholder="Numse"
                required></b-form-input>
            </b-form-group>
  
            <b-button type="submit" variant="primary">Submit</b-button>
            <b-button type="reset" variant="danger">Reset</b-button>
          </b-form>
        </b-col>
      </b-row>
    </b-container>
  </template>
   
  <script>
  export default {
    data() {
      return {
        form: {
          marca: '',
          modelo: '',
          año: '',
          numse: '',
        },
        show: true,
      };
    },
    methods: {
      onSubmit() {
        
        if (!this.form.marca || !this.form.modelo || !this.form.año || !this.form.numse) {
          alert('Completa todos los campos, por favor =).');
          return;
        }
  
        alert('Enviando formulario =) ...');
  
        this.onReset();
      },
      onReset() {
        this.form = {
          marca: '',
          modelo: '',
          año: '',
          numse: '',
        };
      },
    },
  };
  </script>
  