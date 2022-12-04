<script setup>
    const navIsOpen = ref(false)
</script>

<template>
    <div>
        <div v-if="navIsOpen" class="fixed top-0 w-screen p-4 text-center shadow-xl bg-neutral-800 h-3/5">
            <MobNav @close="navIsOpen = !navIsOpen" />
        </div>
        <div class="h-12 shadow-lg flex justify-between items-center p-4">
            <div class="font-bold italic tracking-widest">
                <NuxtLink to="/">
                    <span class="text-red-700">FLAT</span>SHIFTERS
                </NuxtLink>
            </div>
            <div  class="md:hidden">
                <button v-if="!navIsOpen">
                    <Icon name="ic:baseline-menu" class="text-2xl hover:text-red-700" @click="navIsOpen = !navIsOpen" />
                </button>
                <button v-if="navIsOpen">
                    <Icon name="ic:close" class="text-2xl" @click="navIsOpen = !navIsOpen" />
                </button>
            </div>
            <div class="hidden md:block">
                <MainNav />
            </div>
        </div>
    </div>
</template>