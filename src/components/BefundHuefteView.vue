<template>
  <div>
    <div v-if="menu == MENU.STARTPAGE">
      <h1>Einschränkungen?</h1>
      <div class="">
        <button @click="menu = MENU.KM" type="button" class="btn btn-secondary">Ja</button>
        <button @click="menu = MENU.ENO" type="button" class="btn btn-secondary">Nein</button>
      </div>
    </div>
    <div v-if="menu == MENU.KM">
      <div class="pointer" @click="menu = MENU.ART">
        <p>
          KM<br />
          IR>Flex+Abd+Ext
        </p>
      </div>
      <div @click="menu = MENU.KKM"><p>KKM</p></div>
    </div>
    <div v-if="menu == MENU.ART">
      <div><p>Arthrose E>S</p></div>
      <div><p>Arthritis S>E</p></div>
    </div>
    <div v-if="menu == MENU.KKM">
      <div>
        <h3 class="text-decoration-underline">Epiphyseolysis capitis femoris (10-14 J.)</h3>
        <ul>
          <li>E+ nicht im KM</li>
        </ul>
      </div>
      <div>
        <h3 class="text-decoration-underline">Corpus liberum</h3>
        <ul>
          <li>Alle E+ möglich o. keine E+</li>
        </ul>
      </div>
      <div>
        <h3 class="text-decoration-underline">“Sign of Buttock”</h3>
        <ul>
          <li>Passive Hüftflexion mit Knieext. E+ S+ (Pseudlaseque)</li>
          <li>Passive Hüftflexion E++ S++</li>
        </ul>
      </div>
    </div>
    <div v-if="menu == MENU.ENO">
      <div>
        <h3>Schnellende Hüfte Bursitis iliopectinea</h3>
        <ul>
          <li>Passive Flexion S+</li>
          <li>Passive AR S+</li>
          <li>Passive Flexion zur gegenüberliegenden Schulter S+++</li>
          <li>evtl. Passive Extension S+</li>
          <li>evtl. Isometrische Flexion S+</li>
        </ul>
      </div>
      <div>
        <h3>Howship-Romberg-Phänomen</h3>
        <p>Einklemmung N. obturatorius</p>
        <ul>
          <li>Passive Abduktion (Knieext.) S+</li>
          <li>Passive Abduktion (Knieflex) negativ</li>
          <li>Isometrische Abduktion negativ</li>
        </ul>
      </div>
      <div>
        <h3>Bursitis subtrochanterica</h3>
        <ul>
          <li>Passive Adduktion S+</li>
          <li>Passive Flexion S+</li>
          <li>Passive AR S+</li>
          <li>Isometrische Abduktion S+</li>
        </ul>
      </div>
      <div>
        <h3>Bursitis Ischiadica</h3>
        <ul>
          <li>evtl. Isometrische Knieflexion S+</li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    const MENU = {
      STARTPAGE: 0,
      KM: 1,
      ART: 2,
      KKM: 3,
      ENO: 4,
    };
    return {
      MENU,
      menu: MENU.STARTPAGE,
    };
  },
};
</script>
<style></style>
