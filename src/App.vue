<script setup>
import ourTeams from './components/ourTeams.vue'; 
import { ref ,  reactive } from 'vue';

const teams = reactive([
  {
    name: 'Team 1',
    members: [
      {
        name: 'Member 1',
        role: 'Role 1',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 2',
        role: 'Role 2',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 3',
        role: 'Role 3',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 4',
        role: 'Role 4',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.' 
      },
    ]
  },
  {
    name: 'Team 2',
    members: [
      {
        name: 'Member 1',
        role: 'Role 1',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 2',
        role: 'Role 2',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 3',
        role: 'Role 3',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 4',
        role: 'Role 4',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
    ]
  },
  {
    name: 'Team 3',
    members: [
      {
        name: 'Member 1',
        role: 'Role 1',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 2',
        role: 'Role 2',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 3',
        role: 'Role 3',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
      {
        name: 'Member 15',
        role: 'Role 4',
        image: 'https://picsum.photos/200/300',
        description: 'Lorem ipsum dolor sit am et, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo.'
      },
    ]
  }
]);


</script>

<template>

  <template v-for="team , index in teams" :key="index">
    <ourTeams :members="team.members" :name="team.name" />
  </template>
</template>

<style scoped>

</style>
