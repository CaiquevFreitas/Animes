<script setup>
    const props = defineProps(['link','title'])
</script>

<template>
    <button class="bg-white hover:bg-blue-400 duration-300 w-80 h-10 rounded-sm">
        <a class="py-2 px-30 font-sans text-xl" :href=props.link>{{props.title}}</a>
    </button>
</template>