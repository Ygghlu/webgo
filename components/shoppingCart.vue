

<template>
    <div class="offcanvas offcanvas-top" 
         tabindex="-1" 
         id="offcanvasTop" 
         aria-labelledby="offcanvasTopLabel">

    <div class="offcanvas-header">
        <h5 id="offcanvasTopLabel">Offcanvas top</h5>

        <button type="button" 
                class="btn-close text-reset" 
                data-bs-dismiss="offcanvas" 
                aria-label="Close"></button>
    </div>

  <div class="offcanvas-body">
    ...
  </div>
</div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    setup() {
        
    },
    mounted() {
    /// Retrieves cart from local storage when user first loads

    this.shoppingCart = JSON.parse(
        localStorage.getItem('shoppingCart') || "[]")

},
})
</script>
