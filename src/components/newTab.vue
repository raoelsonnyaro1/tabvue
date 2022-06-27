<template>
    <table>
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
}</style>