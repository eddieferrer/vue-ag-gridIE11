<template>
    <ag-grid-vue
      class="ag-theme-balham"
      :columnDefs="columnDefs"
      :rowData="rowData"
    >
      >
    </ag-grid-vue>
</template>

<script>
import { AgGridVue } from "ag-grid-vue";

export default {
  name: "HelloWorld",
  components: { AgGridVue },
  data() {
    return {
      columnDefs: null,
      rowData: null
    };
  },
  beforeMount() {
    this.columnDefs = [
      { headerName: "Make", field: "make" },
      { headerName: "Model", field: "model" },
      { headerName: "Price", field: "price" }
    ];

    this.rowData = [
      { make: "Toyota", model: "Celica", price: 35000 },
      { make: "Ford", model: "Mondeo", price: 32000 },
      { make: "Porsche", model: "Boxter", price: 72000 }
    ];
  }
};
</script>

<style scoped>
</style>
