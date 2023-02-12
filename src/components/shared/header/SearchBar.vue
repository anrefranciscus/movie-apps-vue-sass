<template>
  <input
      type="search"
      placeholder="Search 🔎"
      class="search"
      name="q"
      autocomplete="off"
  />
</template>

<script>
export default {
  name: "SearchBar"
}
</script>

<style lang="scss" scoped>
@import "@/assets/style/__variables.scss";
.search {
  padding: 1rem;
  border: 0;
  border-radius: 0;
  outline: 0;
  &:focus {
    color: #fff;
    background: $green;
    outline: 1px solid #fff;
  }
  &:focus::placeholder {
    color: #fff;
  }
}
</style>
