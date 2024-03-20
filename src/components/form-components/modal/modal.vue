<script lang="ts">
export default {
props:['color','message','isAktif'],
data() {
     return{
        active : false
     }
 },
 methods:{
    modal_active(){
        this.$emit('modal-active',this.active)
    }
 }
}
</script>

<template>
    <!-- Snackbar -->
    <VSnackbar :v-model="isAktif" :variant="color" transition="scroll-y-reverse-transition" location="top end"
        :timeout="2000">
        {{ message }}
    </VSnackbar>
</template>