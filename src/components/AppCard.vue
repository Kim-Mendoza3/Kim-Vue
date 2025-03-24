<template>
    <div class="card p-4 mb-3" style="width: 80rem; text-align: center;">
          <div class="card-body">
            <!-- Primera fila con 2 tarjetas -->
            <div class="row row-cols-1 row-cols-md-2 g-3 mb-3">
              <div class="col" v-for="(image, index) in images.slice(0, 2)" :key="index">
                <div class="card h-100">
                  <div class="card-header text-white" style="background-color: orange;">
                    <h6 class="text-center">CARD</h6>
                  </div>
                  <div class="card-body text-center">
                    <img :src="image.src" class="card-img-top rounded-circle mx-auto mt-3" style="width: 150px; height: 150px;" alt="Imagen">
                    <p style="font-style:italic;">{{ image.text }}</p>
                    <a href="#" class="btn btn-primary" style="background-color: brown;">Watch Serie</a>
                  </div>
                </div>
              </div>
            </div>
            <!-- Segunda fila con 3 tarjetas -->
            <div class="row row-cols-1 row-cols-md-3 g-3">
              <div class="col" v-for="(image, index) in images.slice(2, 5)" :key="index">
                <div class="card h-100">
                  <div class="card-header text-white" style="background-color: orange">
                    <h6 class="text-center">CARD</h6>
                  </div>
                  <div class="card-body text-center">
                    <img :src="image.src" class="card-img-top rounded-circle mx-auto mt-3" style="width: 150px; height: 150px;" alt="Imagen">
                    <p style="font-style:italic;">{{ image.text }}</p>
                    <a href="#" class="btn btn-primary" style="background-color: brown;">Watch Serie </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
    </template>
    
    
    <script>
    export default {
      data() {
        return {
          images: [
            { src: "https://m.media-amazon.com/images/I/51OCvr4r0CL._AC_UF894,1000_QL80_.jpg", text: "El canario Piolín y el gato Silvestre aparecen juntos, con Piolín en primer plano y Silvestre detrás, mirando con una expresión curiosa." },
            { src: "https://la100.cienradios.com/resizer/P30OCfWqPYjM5BVsYW9abkGkCW0=/arc-photo-radiomitre/arc2-prod/public/FXJGPTKJQZFULA3NF6D5Y6YPXE.jpg", text: " Silvestre salta hacia Piolín con una expresión agresiva, mientras Piolín parece pequeño y en peligro." },
            { src: "https://i.pinimg.com/474x/8a/f8/95/8af89547044a6f3eec4d49707fcc54b4.jpg", text: "Piolín usa patines y se mueve con energía, mientras Silvestre lo sigue con una expresión divertida." },
            { src: "https://i.pinimg.com/originals/02/0f/8b/020f8b63343859ac6a00512e07a118a9.png", text: "Piolín y Silvestre aparecen caminando juntos, con Silvestre mostrando una actitud amigable." },
            { src: "https://i.pinimg.com/236x/a5/e2/e9/a5e2e945b31c685c58d4b8edb4ab952d.jpg", text: "Silvestre luce orgulloso con los brazos cruzados mientras Piolín sostiene una copa o trofeo, representando una victoria." }
          ]
        };
      }
    };
    </script>