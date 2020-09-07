<template>
  <div>
    <px-assets-table :assets="assets" />
  </div>
</template>

<script>
import api from "@/api";
import PxAssetsTable from "@/components/PxAssetsTable";

export default {
  name: "Home",
  components: { PxAssetsTable },

  // Propiedad
  data() {
    return {
      assets: []
    };
  },

  // Se ejecuta cuando se crea el componente para hacer la interaccion con la API
  created() {
    api.getAssets().then(assets => (this.assets = assets));
  }
};
</script>
