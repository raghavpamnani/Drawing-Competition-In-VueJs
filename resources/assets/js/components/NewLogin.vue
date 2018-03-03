<template>
  <form>
    <v-text-field
      label="Name"
      v-model="name"
      required
    ></v-text-field>
    <v-text-field
      label="E-mail"
      v-model="email"
      required
    ></v-text-field>
    <v-select
      label="Item"
      v-model="select"
      required
    ></v-select>
    <v-checkbox
      label="Do you agree?"
      v-model="checkbox"
      required
    ></v-checkbox>

    <v-btn>submit</v-btn>
    <v-btn>clear</v-btn>
  </form>
</template>

