<template>
    <table class="mx-auto">
        <th colspan="2">newTab</th>
        <tr>
            <td>nom complet niova:</td>
            <td>{{newValeur}}</td>
        </tr>
    </table>
</template>

<script>
export default {
  name: 'oldTab',
  props: {
    newValeur: String,
    default:"",
  }
}
</script>

<style>
table{
  border-collapse: collapse;
}

th, td{
  border: 1px solid black;
  padding: 10px;
}

.mx-auto{
    margin-left: auto;
    margin-right: auto;
}
</style>