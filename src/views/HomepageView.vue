<template>
  <div class="pozadinaStranice">
    <div class="stranicaHomePageIzgled">
      <h1>Pixel Art</h1>

      <p class="uvodTekst">
        Pixel Art je sajt namenjen za kolaborativno ili samostalno crtanje i deljenje crteža.
        Pogledajte našu galeriju i počnite već sami da svoje ideje pretvorite u deo toga!
      </p>
      
      <div class="carouselSlideovi mb-5">
        <div id="carouselExampleContent" class="carousel slide" data-bs-ride="carousel" data-bs-autoplay="true" data-bs-interval="3000">
          <div class="carousel-inner rounded-5">
            
            <div class="carousel-item active" data-bs-interval="3000">
              <div class="d-flex flex-column justify-content-center text-start bg-subtle-primary p-5 bg-1 rounded-5 slideoviIzgled slideCrtanje">
                <h3 class="slideoviNaslov">Pustite maštu na volju!</h3>
                <p class="slideoviOpis mb-3">Počni i TI da širiš svoje ideje i kreativnost, i postani deo naše velike Pixel Art zajednice</p>
                <div class="dugmiciSaSlideova">
                  <RouterLink to="/crtanje" class="btn slideDugmici crtanjeDugme">Počni sa crtanjem</RouterLink>
                </div>
              </div>
            </div>
            
            <div class="carousel-item" data-bs-interval="3000">
              <div class="d-flex flex-column justify-content-center text-center bg-subtle-success p-5 bg-2 rounded-5 slideoviIzgled slideGalerija">
                <h3 class="slideoviNaslov">Galerija - tvoje mesto za ideju i inspiraciju</h3>
                <p class="slideoviOpis mb-2">Želiš da inspirišeš svoju kreativnost i ideje, ili imaš već postojeće koje nisu ugledale svetlost dana?</p>
                <p class="slideoviOpis mb-3">Pogledaj našu galeriju, upotpuni svoju inspiraciju i postani deo naše galerije</p>
                <div class="dugmiciSaSlideova">
                  <RouterLink to="/gallery" class="btn slideDugmici galerijaDugme">Pogledaj galeriju</RouterLink>
                </div>
              </div>
            </div>
            
            <div class="carousel-item" data-bs-interval="3000">
              <div class="d-flex flex-column justify-content-center text-end bg-subtle-warning p-5 bg-3 rounded-5 slideoviIzgled slideRegister">
                <h3 class="slideoviNaslov">Postani član Pixel Art zajednice!</h3>
                <p class="slideoviOpis mb-3">Nisi još uvek prijavljen? Postani već sada i saznaj prvi o našim budućim pogodnostima i promenama samo za prijavljene članove</p>
                <div class="dugmiciSaSlideova">
                  <RouterLink to="/register" class="btn slideDugmici registerDugme">Registruj nalog</RouterLink>
                </div>
              </div>
            </div>
            
          </div>
          
          <div class="d-flex justify-content-center gap-3 mt-4 promeniSlide">
            <button class="sledeciSlideDugmici" type="button" data-bs-target="#carouselExampleContent" data-bs-slide="prev">
              <span aria-hidden="true">&lt;</span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button class="sledeciSlideDugmici" type="button" data-bs-target="#carouselExampleContent" data-bs-slide="next">
              <span aria-hidden="true">&gt;</span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
        </div>
      </div>

      <div class="container-fluid opisSajta">
        <div class="row">
          <div class="col-md-6">
            <p class="opisSajtaTekst">
              Sed faucibus dictum varius. Nullam id placerat eros. Pellentesque molestie aliquet nisl, facilisis dignissim tortor egestas quis. Nulla vel enim et dolor vehicula laoreet a a augue. Fusce at rhoncus elit. Pellentesque fermentum odio sed eros venenatis, eget condimentum nisl tempus. Integer suscipit neque in elit posuere, nec feugiat tortor tempor. In nec maximus ligula, et suscipit ante. Nunc justo nisl, congue in nunc id, vehicula fermentum nisl. Pellentesque ac lectus purus.
            </p>
          </div>
          <div class="col-md-6">
            <p class="opisSajtaTekst">
              Interdum et malesuada fames ac ante ipsum primis in faucibus. Nam sollicitudin pretium felis non tempus. Nulla in ex placerat, dictum augue in, ultrices nibh. Maecenas iaculis libero ut ante aliquam, in feugiat sem porttitor. Fusce commodo purus eros, sit amet ullamcorper libero placerat ut. Sed a congue mi. Nulla quis tortor facilisis, tempus nisl non, placerat sapien. Donec eget elementum dolor. Aenean auctor laoreet imperdiet. Fusce quis nunc ac orci scelerisque hendrerit nec at turpis. Aenean aliquet est vel magna facilisis, vel facilisis lacus pellentesque. 
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<style scoped>
.pozadinaStranice {
  min-height: 100vh;
  background-image: url('@/assets/pozadina.jpg');
  background-size: cover;
  background-position: center;
}

.stranicaHomePageIzgled {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 1400px;
  margin: 0 auto;
  padding: 30px 20px;
  text-align: center;
}

h1 {
  font-size: 2.5rem;
  color: #1f2937;
  background-color: rgba(255, 255, 255, 0.9);
  padding: 8px 30px;
  border-radius: 10px;
  margin-bottom: 20px;
}

.uvodTekst {
  font-size: 1.3rem;
  font-weight: 600;
  line-height: 1.7;
  color: #1f2937;
  background-color: rgba(255, 255, 255, 0.9);
  padding: 20px 30px;
  border-radius: 10px;
  margin-bottom: 30px;
}

.carouselSlideovi {
  width: 100%;
  max-width: 1200px; 
}

.slideoviIzgled {
  min-height: 320px;
  font-family: 'Segoe UI', sans-serif;
  color: #1f2937; 
}

.slideCrtanje {
  background-color: #e3f2fd;
}

.slideGalerija {
  background-color: #d1e7dd;
}

.slideRegister {
  background-color: #f8d7da;
}

.slideoviNaslov {
  font-size: 2.2rem;
  font-weight: 700;
  margin-bottom: 15px;
}

.slideoviOpis {
  font-size: 1.15rem;
  color: #1f2937; 
}

.dugmiciSaSlideova {
  margin-top: 50px;
}

.slideDugmici {
  font-weight: 600;
  padding: 12px 30px;
  border-radius: 8px;
}

.crtanjeDugme {
  background-color: #0d6efd;
  color: #e3f2fd; 
}

.galerijaDugme {
  background-color: #198754;
  color: #d1e7dd;
}

.registerDugme {
  background-color: #c1505c;
  color: #f8d7da;
}

.promeniSlide {
  margin-bottom: 80px;
}

.sledeciSlideDugmici {
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background-color: #1f2937; 
  color: #ffffff; 
  font-size: 1.5rem; 
  font-weight: bold;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background-color 0.2s ease-in-out;
  cursor: pointer;
}

.sledeciSlideDugmici:hover {
  background-color: #9a9ca1; 
  color: #ffffff;
}

.opisSajta {
  background-color: rgba(255, 255, 255, 0.9);
  border-radius: 10px;
  margin-bottom: 20px;
}

.opisSajtaTekst {
  font-size: 1.05rem;
  font-weight: 600;
  line-height: 1.8;
  color: #1f2937;
  background-color: rgba(255, 255, 255, 0);
  padding: 25px 35px;
  border-radius: 10px;
  margin: 0 0 20px 0;
  height: 100%;
}
</style>