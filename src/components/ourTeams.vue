<script setup>

import nameEditor from './nameEditor.vue';
import editorForm from './editorForm.vue';
defineProps(
    {
      members: {
        type: Object
      }, 
      name: {
        type: String
      } 
    }
);
  
</script>

<template>
<section class="mx-auto container">
        <section class="bg-white dark:bg-gray-900">
            <div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 lg:px-6 ">
                <div class="mx-auto max-w-screen-sm text-center mb-8 lg:mb-16">
                    <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">{{ name }}</h2>
                    <p class="font-light text-gray-500 lg:mb-16 sm:text-xl dark:text-gray-400">Explore the whole collection of open-source web components and elements built with the utility classes from Tailwind</p>
                </div>
                
               
                    <div class="grid gap-8 mb-6 lg:mb-16 md:grid-cols-2">
                    <div class="items-center bg-gray-50 shadow sm:flex dark:bg-gray-800 dark:border-gray-700" v-for="member , index in members"  :key="index">
                        <a href="#">
                            <img class="w-full  " :src="member.image" :alt="member.name ">
                        </a>
                        <div class="p-5">
                            <h3 class="text-xl font-bold tracking-tight text-gray-900 dark:text-white">
                                <a href="#">{{ member.name }}</a>
                            </h3>
                            <span class="text-gray-500 dark:text-gray-400">{{ member.role }}</span>
                            <p class="mt-3 mb-4 font-light text-gray-500 dark:text-gray-400">{{ member.description }}</p>

                            <editorForm v-model:name="member.name"   v-model:role="member.role" /> 
                            <!-- <nameEditor v-model:name="member.name" /> -->

                        </div>
                    </div>
                </div>
            </div>
        </section>
    </section>
</template>

<style scoped></style>