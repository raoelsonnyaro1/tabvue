<template>
    <table>
        <th colspan="2">oldTab</th>
        <tr>
            <td>nom complet:</td>
            <td>{{valeur}}</td>
        </tr>
    </table>
</template>

<script>
export default {
  name: 'oldTab',
  props: {
    valeur: String,
    default:"",
  }
}
</script>

<style>

</style>