<template>
    <div class="container">
        <div class="row mt-4">
        <div>
            <h4 style="color: blue; font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;">EVENTO CLICK</h4>
        <button @click="clic" class="btn btn-danger" type="button">Da Click</button> 
        <button @click="soyboton" class="btn btn-warning mx-2" type="button">Da Click</button> 
    </div>
    <div>
            <h4 style="color: greenyellow; font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;">EVENTO CHANGE</h4>
            <label class="input-group-text" for="">Ingresa tu nombre</label>
            <input class="form-control mt-2" type="text" id="nombre" @change="nombreE">
           <p> El nombre ingresado es: <strong>{{ nombre }}</strong></p> 
    </div>
 <div>
    <h4 style="color: red; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;">EVENTO MENSAJES</h4>
    <div style="width: 1100px;height: 200px; background-color: purple;text-align: center;padding: 15px;border-radius: 14px;" 
    @mouseenter="mostrarmensaje" @mouseleave="ocultarmensaje">
    <p class="text-center text-white">Pase el Mouse</p>
    <p class="text-white">{{ mensaje }}</p>


    </div>

 </div>
   

</div>   
</div>
</template>
<script>
export default {
    data(){
return{
    nombre:'',
    mensaje:'',
}
    },
    methods:{
        clic(){
            alert("gracias por darle click")
        },
        soyboton(){
            alert("soy un boton!!")
        },
        nombreE(event){
this.nombre = event.target.value
        },
        mostrarmensaje(){
            this.mensaje="el mouse esta dentro del cuadro"
            
        },
        ocultarmensaje(){
    this.mensaje="el raton esta fuera del cuadro"
        }

    }

}
</script>
<style>
.fondo {
    background-color: aquamarine; /* Color de fondo claro */
    min-height: 100vh; /* Asegura que cubra toda la pantalla */
    padding: 20px; /* Espaciado interno */
}
</style>