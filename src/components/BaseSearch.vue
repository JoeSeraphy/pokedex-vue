<template>
  <div class="w-full flex justify-center mx-auto py-2 bg-gray-700">
    <form @submit="onSubmit">
      <input
        v-model="pokeName"
        type="text"
        name="pokeName"
        placeholder="Digite o nome do Pokémon"
        class="py-3 px-4 w-96 rounded-lg outline-none"
      />
      <button
        class="ml-4 text-white text-xl py-2 px-4 bg-blue-400 rounded-xl"
        type="submit"
      >
        Buscar
      </button>
    </form>
  </div>
</template>

<script>
export default {
  name: "BaseSearch",
  data() {
    return {
      pokeName: "",
    };
  },
  methods: {
    onSubmit(e) {
      console.log("enter", e);
      this.$emit("search_pokeName", this.pokeName);
    },
  },
};
</script>
