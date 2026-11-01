<template>
  <div class="pozadinaStranice">
    <div class="stranicaCrtanjeIzgled">
      <div class="panelSaAlatima">
        <span>Alat: Olovka ✏️</span>
        <label for="bojaAlata">Izbor boje:</label>
        <input id="bojaAlata" type="color" v-model="odabranaBoja" />
      </div>

      <div class="platnoZaCrtanje" draggable="false">
        <div v-for="(redPixela, i) in platno" :key="i" class="redoviSaPixelima">
          <div
            v-for="(bojaPixela, j) in redPixela"
            :key="j"
            class="pixel"
            :style="{ backgroundColor: bojaPixela }"
            @mousedown="obojiPixel(i, j)"
            @mouseenter="obojiPrevlacenjemMisaPixel(i, j, $event)"
          ></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  import { ref } from 'vue'

  const brojRedova = 30
  const brojKolona = 50

  let odabranaBoja = ref('#000000')
  const platno = ref<string[][]>([])

  function kreirajPlatno() {
    for (let i = 0; i < brojRedova; i++) {
      let redPixela: string[] = [] 
    
      for (let j = 0; j < brojKolona; j++) {
        redPixela.push('#ffffff')
      }

      platno.value.push(redPixela)
    }
  }

  let obojiPixel = (i: number, j: number) => {
    platno.value[i][j] = odabranaBoja.value
  }

  let obojiPrevlacenjemMisaPixel = (i: number, j: number, dogadjajSaMisa: MouseEvent) => {
    if (dogadjajSaMisa.buttons === 1) {
      platno.value[i][j] = odabranaBoja.value
  }
}

  kreirajPlatno()
</script>

<style scoped>
  .pozadinaStranice {
    min-height: calc(100vh - 60px);
    width: 100%;
    background-image: url('@/assets/pozadina.jpg');
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    padding: 40px 20px;
    box-sizing: border-box;
  }

  .stranicaCrtanjeIzgled {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .panelSaAlatima {
    display: flex;
    align-items: center;
    gap: 15px;
    margin-bottom: 20px;
    padding: 10px 20px;
    font-weight: 600;
    color: #1f2937;
    background-color: rgba(255, 255, 255, 0.92);
    border-radius: 10px;
  }

  .platnoZaCrtanje {
    border: 10px solid #666;
    background-color: white;
    user-select: none;
  }

  .redoviSaPixelima{
    display: flex;
  }

  .pixel {
    width: 22px;
    height: 22px;
    box-sizing: border-box;
    border: 1px solid #ddd;
    cursor: pointer;
  }
</style>