<template>
    
     <div class="modal fade" id="Modal_1" tabindex="-1" aria-labelledby="#exampleModalLabel1" aria-hidden="true">
             <div class="modal-dialog">
                 <div class="modal-content">
                 <div class="modal-header">
                 <h5 class="modal-title" id="exampleModalLabel1">{{character.name}}</h5>
                 <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
             <div class="modal-body">

              

                <img :src="character.thumbnail"
                     :alt="character.name" 
                     class="img-fluid rounded-start">

                <div>
                  <p class ="text-muted">{{character.modified}}</p>
                  <h5>Описание:</h5>
                  <p>
                    {{character.description}}
                  </p>
                  <h5>Комиксы:</h5>
                   <ul>
                    <li v-for="(el, idx) in character.comics"
                        :key="idx"
                    >{{el.name}}</li> 
                    
                   </ul>
                </div>
                </div>
             <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Закрыть</button>
             </div>
             </div>
            </div>
            </div>

</template>

<script>
    export default {
        name: "AppModal",
        props: ["character"]
    }
</script>

<style scoped>

</style>
