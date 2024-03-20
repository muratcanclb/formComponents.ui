<template>
  <div>
    <VCard title="Create Alert Page 🙌">
      <VCardText>This is your alert page.</VCardText>
      <VCardText>
        Chocolate sesame snaps pie carrot cake pastry pie lollipop muffin.
      </VCardText>
    </VCard>
    <VCard v-for="i in AlertProperty" key="color">
      <Alert :data="i"></Alert>
    </VCard>
    <VBtn @click="isVisible = !isVisible">
        Doğrula
    </VBtn>
    <VCard>
      <Modal :isAktif="isVisible" color="success" message="BAŞARILI"></Modal>
    </VCard>
  </div>
</template>

<script>
import Alert from '@/components/form-components/alert/alert.vue';
import Modal from '../components/form-components/modal/modal.vue';
export default {
  components: {
    Alert,
    Modal
  },
  data(){
    return{
      AlertProperty:[
        {color:"primary",message:"Nullam tincidunt adipiscing enim. In consectetuer turpis ut velit."},
        {color:"secondary",message:"Nullam tincidunt adipiscing enim. In consectetuer turpis ut velit."},
        {color:"success",message:"Nullam tincidunt adipiscing enim. In consectetuer turpis ut velit."},
        {color:"info",message:"Nullam tincidunt adipiscing enim. In consectetuer turpis ut velit."},
        {color:"error",message:"Nullam tincidunt adipiscing enim. In consectetuer turpis ut velit."},
      ],
      isVisible:false
    }
  }
};
</script>
