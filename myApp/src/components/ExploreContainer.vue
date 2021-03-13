<template>
<ion-content>
  <ion-card id="card" v-for="(item, index) in APIData" :key="index">
    <ion-card-header>
      <ion-card-title>{{item.title}}</ion-card-title>
      <ion-card-subtitle>{{item.Company}}  |  {{item.salary}}</ion-card-subtitle> 
    </ion-card-header>

    <ion-card-content>
      {{item.description}}
    </ion-card-content>
    <ion-button target="_blank" :href="item.Contact" id="btn" color="success">Acessar</ion-button>
        <ion-button to="/tab2222" id="btn" color="primary">Informações</ion-button>
  </ion-card>
</ion-content>
</template>

<script>
import { getAPI } from "@/axio-api";
export default {
  data() {
    return {
      APIData: []
    };
  },
  created() {
    getAPI
      .get("/jobs/")
      .then(response => {
        console.log("Post api is getting data");
        this.APIData = response.data;
      })
      .catch(err => {
        console.log(err);
      });
  }
};
</script>

<style scoped>
#btn {
  margin: 10px;
}
#card {
  margin-bottom: 20px;
}
</style>