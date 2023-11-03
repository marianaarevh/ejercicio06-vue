<template>
    <h1>Formulario de Contacto</h1>
    <div id="contendedor-formulario">

        <form id="formulario">
            <input type="text" id="nombre" placeholder="Nombre" required>
            <input type="email" id="email" placeholder="Email" required>
            <textarea id="mensaje" placeholder="Mensaje" required></textarea>
            <button id="btn-enviar" type="submit" class="btn">Enviar <i class="fa-regular fa-envelope"></i></button>
        </form>
    </div>
</template>

<script>
 export default {
      name: 'ContactForm',
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
</style>