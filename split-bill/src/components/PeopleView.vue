<script setup>
import {store, getGrandTotal} from '../store/store';
import Label from "@/components/Label.vue";
</script>

<template>
  <div class="no-items" v-if="store.people.length === 0">No items</div>
  <div class="people-view" v-if="store.people.length > 0">
    <div class="header">
      <div>
        <Label title="Total + Tip: " :value="getGrandTotal" />
      </div>
      <div>
     <Label title="Remaining: " :value="store.params.remaining" />
      </div>
    </div>

    <div class="people-container">
      <div v-for="person in store.people" :key="person.id">
        {{person.totalPerPerson}}
      </div>
    </div>
  </div>
</template>

<style scoped></style>