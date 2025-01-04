<template>
  <q-page padding>
    <q-table :columns="columns" :rows="users"></q-table>
  </q-page>
</template>

<script setup lang="ts">
import type{ User } from 'src/models';
import { ref } from 'vue';
import type{ QTableColumn } from 'quasar';

const columns:QTableColumn[] = [
  {
    name: 'id',
    label: 'ID',
    field: 'id',
    align: 'center',
    sortable:true,
  },
  {
    name: 'email',
    label: 'Email',
    field: 'email',
    align: 'center',
  },
  {
    name: 'password',
    label: 'Password',
    field: 'password',
    align: 'center',
  }
]

const users = ref<User[]>([
  {
    id: 1,
    email:'admin@mail.com',
    password: 'Pass@1234'
  },
  {
    id: 2,
    email:'user@mail.com',
    password: 'Pass@1234'
  }
])
// let lastUserId = 3
</script>
