<script setup>
    import ButtonLinkPages from '../components/ButtonLinkPages.vue';
</script>

<template>
    <div class="bg-black w-screen h-screen">
        <div class="text-center">
            <h1 class="text-white text-7xl p-20">Meus animes</h1>
        </div>
        <div class="flex justify-center items-center flex-col gap-8">
            <ButtonLinkPages link="#/ListadeAnimes" title="Lista"/>
            <ButtonLinkPages link="#/CadastrodeAnimes" title="Cadastrar"/>
            <ButtonLinkPages link="#/EditarAnimes" title="Editar"/>
        </div>  
    </div>

</template>


