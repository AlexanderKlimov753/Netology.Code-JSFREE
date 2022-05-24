<template>
    <nav class="navbar navbar-dark bg-dark">
        <div class="container-fluid">
          <a class="navbar-brand">Marvel</a>
          <form class="d-flex">
            <input class="form-control me-2" 
              type="search" 
              placeholder="Поиск..." 
              aria-label="Search"
              v-model="search"
              @input="characterSearch(search)"
              >
            <button 
              class="btn btn-outline-light" 
              type="submit"
               @click="()=>{search=''; changeSearch(search)}"
              >
              Все
            </button>
          </form>
        </div>
    </nav>
</template>

<script>
    export default {
        name: "AppHeader",
        props: ["characterSearch"],
        data() {
            return {
                search: "",
            }
        },
    }
</script>

<style scoped>

</style>
