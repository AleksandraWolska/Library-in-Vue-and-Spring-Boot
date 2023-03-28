<template>
  <div id="persons-table">
    <table>
      <thead>
        <tr>
          <th>Imię i nazwisko</th>
          <th>email</th>
          <th>telefon</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="person in personsSource" :key="person.id">
          <td>{{ person.name }}</td>
          <td>{{ person.email }}</td>
          <td>{{ person.phone }}</td>
        </tr>

        <tr>
          <td>Jan Kowalski</td>
          <td>jan.kowalski@example.pl</td>
          <td>+48 603-788-987</td>
        </tr>
        <tr>
          <td>Maria Koniuszy</td>
          <td>m.kon@example.com</td>
          <td>+48 730-889-966</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>


<script>
export default {
  name: "PersonsTable",
  props: {
    personsSource: Array,
  },
};
</script>
<style scoped></style>