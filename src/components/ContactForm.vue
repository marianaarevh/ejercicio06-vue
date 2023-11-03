<template>
    <h1>Formulario de Contacto</h1>
    <div id="contendedor-formulario">

        <form id="formulario" @submit="validateForm">
            <input type="text" name="nombre" placeholder="Nombre" v-model="nombre">
            <input type="email" name="email" placeholder="Email" v-model="email">
            <textarea v-model="mensaje" name="mensaje" placeholder="Mensaje"></textarea>
            <button id="btn-enviar" type="submit" class="btn">Enviar <i class="fa-regular fa-envelope"></i></button>
        </form>
    </div>
    <ul>
        <h5> Recursos utilizados: </h5>
        <li> <a href="https://es.vuejs.org/v2/cookbook/form-validation"> https://es.vuejs.org/v2/cookbook/form-validation </a></li>
        <li><a href="https://areimilla.cl/site/blog-post/validacion-de-un-formulario-con-vue-js/"> https://areimilla.cl/site/blog-post/validacion-de-un-formulario-con-vue-js/ </a></li>
    </ul>
</template>

<script>
 export default {
    name: 'ContactForm',
    data() {
        return {
            formData: {
                nombre: null,
                email: null,
                mensaje: null
            }
        }
    },

    methods:{
        validateForm: function(e){
            if(!this.nombre){
                alert("Debes agregar el nombre.");
                e.preventDefault();
            }

            if (!this.email) {
                alert('Debes agregar un correo electrónico.');
            }
            
            if(!this.mensaje){
                alert("Debes agregar un mensaje.");
            e.preventDefault();
            }

            if(this.mensaje && this.mensaje.length <5){
                alert("El mensaje contener más de 5 caracteres.");
            e.preventDefault();
            }
        }
        }
 }
</script>

<style>
#contendedor-formulario {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
}

#formulario {
  display: flex;
  flex-direction: column;
  width: 600px;
}

input, textarea {
  font-size: 1rem;
  border-bottom:1px solid #0079FF;
  padding: 10px;
  margin: 5px;
  border-radius: 10px;

}

#btn-enviar{
  color: #f0f0f0;
  background-color:#0079FF;
  border-radius: 10px;
  font-size: 1rem;
  font-weight: 700;
  padding: 5px;
  margin: 5px;
  

}

#btn-enviar:hover{
  background-color:rgb(0, 104, 224);
}

li{
    list-style: none;
}
</style>