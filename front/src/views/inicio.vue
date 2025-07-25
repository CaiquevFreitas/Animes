<script setup>
    import ButtonLinkPages from '../components/ButtonLinkPages.vue';
</script>

<template>
    <div class="bg-black w-screen h-screen flex justify-center items-center flex-col gap-8">
            <ButtonLinkPages link="#/ListadeAnimes" title="Lista"/>
            <ButtonLinkPages link="#/CadastrodeAnimes" title="Cadastrar"/>
            <ButtonLinkPages link="#/EditarAnimes" title="Editar"/>
    </div>  
</template>


