<template>
<VLayout>
    <template #header>
        <VHeader>
            <template #start>logo</template>
        </VHeader>
    </template>


    <template #side-bar>
        <div class="bg-secondary col-2 p-4">sidebar</div>
    </template>

    <template #default>
        <router-view/>
    </template>

    <template #footer>
        footer
    </template>


</VLayout>
</template>

<script setup>
import VHeader from "@/components/layout/VHeader.vue";
import VLayout from "@/components/layout/VLayout.vue";
</script>
