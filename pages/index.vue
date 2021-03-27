<template>
  <div class="flex flex-col space-y-3 px-4">
    <h2 class="text-3xl">
      ¿Por quién votar estas elecciones generales del 11 de Abril del 2021?
    </h2>
    <div>
      <a
        href="https://www.onpe.gob.pe/modElecciones/elecciones/2021/EEGG/doc/miembro-mesa/como-votar-nacional.pdf"
        >¿Cómo votar?</a
      >
      <a href="https://www.consultamiembrodemesa.eleccionesgenerales2021.pe/#/"
        >¿Dónde voto?</a
      >
    </div>
    <div class="flex space-x-2">
      <p class="text-red-500">Presidentes</p>
      <p>Congresistas</p>
      <p>Partido Andino</p>
    </div>
    <div>
      <a
        href="https://es.wikipedia.org/wiki/Juntos_por_el_Per%C3%BA"
        class="text-3xl font-bold"
        >Juntos por el Perú</a
      >
      <div class="flex">
        <img
          class="object-contain "
          src="~/assets/veronika_mendoza.png"
          alt="Juntos por el Peru y Veronika Mendoza"
        />
        <div class="flex flex-col">
          <a href="https://twitter.com/Vero_Mendoza_F">Verónika Mendoza</a>
          <p class="text-xs text-gray-400">Candidata presidencial</p>
          <a
            href="https://apisije-e.jne.gob.pe/TRAMITE/ESCRITO/1587/ARCHIVO/FIRMADO/5262.PDF"
            >Plan de gobierno</a
          >
          <a href="https://www.instagram.com/p/CM4t88TJw_V/"
            >Propuestas notables</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async mounted() {
    const data = await this.$strapi.graphql({
      query: `
    query {
      organizations {
        name
      }
    }
  `
    });

    console.log(data);
  }
};
</script>

<style></style>
