<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import axios from "axios";
import { store } from "./store";

export default {
  components: {
    AppHeader,
    AppMain,
  },
  data() {
    return {
      store
    }
  }, 
/*   methods: {
    cardsFilter() {
      if (this.store.filterArchitype) {
        params.archetype = this.store.filterArchitype;
      }
    }
  }, */
  mounted() {
    this.store.loading = true;
    axios.get(store.apiURL).then((resp) => {
      console.log(resp);
      this.store.characters = resp.data.data;
      this.store.meta = resp.data.meta;
      this.store.loading = false;
    })
  }
}
</script>

<template>
  <AppHeader />
  <AppMain/>
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
