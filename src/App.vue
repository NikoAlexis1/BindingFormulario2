<script>
export default{
  name:"app",
  data(){
    return{
      emoji:"",
      titulo:"",
      apreciacion:"",
      competencias:[],
      opinion:"",
    }
  }
}


</script>

<template>
  <div class="contenedor w-75 m-auto mt-3 d-flex">
    <!-- Formulario Izquierdo -->
    <div class="w-50 bg-dark text-light rounded-4">
      <form class="p-3">
        <div class="row">
          <label class="col-md-12 col-lg-2 col-form-label">Titulo:</label>
          <div class="col-md-12 col-lg-10">
            <input type="text" class="form-control" v-model="titulo">
          </div>
        </div>
        <hr>
        <div class="row">
          <label class="col-md-12 col-lg-2 col-form-label">Emoji:</label>
          <div class="col-md-12 col-lg-3">
            <select class="form-select" v-model="emoji">
              <option value="👩‍💻" Selected>👩‍💻</option>
              <option value="👨‍🎓">👨‍🎓</option>
              <option value="👨‍🏫">👨‍🏫</option>
            </select>
          </div>
        </div>
        <hr>
        <div class="row">
          <label class="col-md-12 col-lg-3">Apreciacion:</label>
          <div class="form-check col-md-6 col-lg-2">
            <input class="form-check-input" name="apreciacion" value="regular" type="radio" v-model="apreciacion">
            <label class="form-check-label">Regular</label>
          </div>
          <div class="form-check col-md-6 col-lg-2">
            <input class="form-check-input" name="apreciacion" value="bien" type="radio" v-model="apreciacion">
            <label class="form-check-label">Bien</label>
          </div>
          <div class="form-check col-md-6 col-lg-2">
            <input class="form-check-input" name="apreciacion" value="muy bien" type="radio" v-model="apreciacion">
            <label class="form-check-label">Muy bien</label>
          </div>
          <div class="form-check col-md-6 col-lg-2">
            <input class="form-check-input" name="apreciacion" value="increible" type="radio" v-model="apreciacion">
            <label class="form-check-label">Increible</label>
          </div>
        </div>
        <hr>
        <div class="row">
          <div class="col-md-12 col-lg-3">
            <label>Competencias aprendidas:</label>
          </div>
          <div class="col-md-12 col-lg-9">
            <div class="form-check col-md-6 col-lg-6 form-check-inline">
              <input class="form-check-input" type="checkbox" value="Morfologia de un componente" v-model="competencias">
              <label class="form-check-label" for="flexCheckDefault">Morfologia de un componente</label>
            </div>
            <div class="form-check col-md-4 col-lg-4 form-check-inline">
              <input class="form-check-input" type="checkbox" value="Directivas" v-model="competencias">
              <label class="form-check-label" for="flexCheckDefault">Directivas</label>
            </div>
            <div class="form-check col-md-6 col-lg-6 form-check-inline">
              <input class="form-check-input" type="checkbox" value="One-Way y Two-Way data binding" v-model="competencias">
              <label class="form-check-label" for="flexCheckDefault">One-Way y Two-Way data binding</label>
            </div>
            <div class="form-check col-md-4 col-lg-4 form-check-inline">
              <input class="form-check-input" type="checkbox" value="Estado" v-model="competencias">
              <label class="form-check-label" for="flexCheckDefault">Estado</label>
            </div>
            <div class="form-check col-md-6 col-lg-6 form-check-inline">
              <input class="form-check-input" type="checkbox" value="El patron de diseño MVVM" v-model="competencias">
              <label class="form-check-label" for="flexCheckDefault">El patron de diseño MVVM</label>
            </div>
          </div>
        </div>
        <hr>
        <div class="row">
          <label class="col-md-12 col-lg-2 col-form-label">Opinion:</label>
          <div class="col-md-12 col-lg-10">
            <textarea class="form-control" cols="3" v-model="opinion"></textarea>
          </div>
        </div>
      </form>
    </div>

    <!-- Valores ingresados derecho-->
    <div class="w-50 ms-3 border rounded-4 text-center">
      <h4>{{ emoji }}</h4>
      <h3>{{ titulo }}</h3>
      <h4>y me parece {{ apreciacion }}</h4>
      <h5>He Aprendido:</h5>
      <h5> {{ competencias }}</h5>
      <h6>Mi opinion hasta ahora del framework es:</h6>
      <p>{{ opinion }}</p>
    </div>
  </div>

</template>

<style scoped>
textarea{
  resize: none;
}
</style>
