<template>
  <div id="slogan">
    <div class="text-center">
      <h1>NameGator</h1>
      <br>
      <h6 class="text-secondary">Gerador de nomes utilizando Vue.js, GraphQL e Node</h6>
    </div>
    <div id="main">
      <div class="container">
        <div class="row">
          <div class="col-md">
            <h5>Prefixos <span class="badge bg-info">{{ prefixes.length }}</span></h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="(prefixe, i) in prefixes" :key="i">
                    {{ prefixe }}
                  </li>
                </ul>
                <br>
                <input type="text" class="form-control" placeholder="Digite o prefixo">
              </div>
            </div>
          </div>
          <div class="col-md">
            <h5>Sufixos <span class="badge bg-info">{{ sufixes.length }}</span></h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="(sufixe, i) in sufixes" :key="i">
                    {{ sufixe }}
                  </li>
                </ul>   
                <br>
                <input type="text" class="form-control" placeholder="Digite o sufixo">             
              </div>
            </div>
          </div>
        </div>
        <br>
        <h5>Domínios <span class="badge bg-info">{{ domains.length }}</span></h5>
        <div class="card">
          <div class="card-body">
            <ul class="list-group">
              <li class="list-group-item" v-for="(domain, i) in domains" :key="i">
                {{ domain }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>    
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css"
import "font-awesome/css/font-awesome.css"

export default {
  name: 'App',
  data() {
    return {
      prefixes: ['Air', 'Jet', 'Flight'],
      sufixes: ['Hub', 'Station', 'Mart'],
      domains: ['AirHub', 'JetStation', 'FlightMart'],
    }
  }
}
</script>

<style>
#slogan {
  margin: 30px 0 30px 0;
}
#main {
  background-color: #F1F1F1;
  padding: 30px 0 30px 0;
}
</style>