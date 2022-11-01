<script>
import InputForm from "@/components/InputForm.vue";
import PeopleView from "@/components/PeopleView.vue";
export default {
  components: {PeopleView, InputForm}
}
</script>

<template>
<div class="container">
<InputForm/>
  <PeopleView/>
</div>
</template>

<style scoped>
.container{
  display: flex;
}
</style>