<template>
  <div class="reason-component">
    <div class="box"></div>
    <button label="Edit" class="edit-button"></button>
  </div>
  <p>Current ilness</p>
  <p>Symptoms:</p>
  <div class="reason-component">
    <div class="box"></div>
    <button label="Edit" class="edit-button"></button>
  </div>
</template>

<script>

export default {
  components: {
  },
  setup() {
    // Aquí puedes agregar la lógica del componente si es necesario
  }
}
</script>

<style scoped>
.reason-component {
  display: flex;
  justify-content: space-between;
}

.box {
  width: 80%;
  height: 200px;
  background-color: #fff;
  border: 1px solid #ddd;
  margin: 10px;
}

p {
  margin: 10px;
}

.edit-button {
  width: 20%;
  height: 40px;
  background-color: #dfcae1;
  color: #000000;
  border: none;
  text-align: center;
  line-height: 40px;
  font-size: 16px;
  margin: 10px;
}
</style>