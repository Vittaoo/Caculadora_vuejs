<script setup> 

    const props = defineProps(['num_1', 'num_2', 'operacao'])

</script>


<template>
    <div class="row d-flex justify-content-center mt-4">
        <div class="col-3">
            <input placeholder="Digite um número" class="form-control p-3 fs-3" type="number" @keyup="props.num_1">
        </div>
      <div class="col-3">
          <input placeholder="Digite um número" class="form-control p-3 fs-3" type="number" @keyup="props.num_2">
      </div>
      <div class="col-4">

          <select class="form-select p-3 fs-3" @change="props.operacao">
            <option value="+">ADIÇÃO</option>
            <option value="/">DIVISÃO</option>
            <option value="*">MULTIPLICAÇÃO</option>
            <option value="-">SUBTRAÇÃO</option>
          </select>
      </div>
    </div>


</template>