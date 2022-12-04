<script setup>
    const emit = defineEmits('close')
</script>

<template>
    <div>
        <div>
            <button class="fixed top-1 right-2" @click="emit('close')">
                <Icon name="mdi:close" class="text-lg hover:text-red-700" />
            </button>
            <ul>
                <li class="hover:underline hover:underline-offset-4 hover:text-red-700">
                    <NuxtLink to="/" @click="emit('close')">
                        Home
                    </NuxtLink>
                </li>
                <li class="hover:underline hover:underline-offset-4 hover:text-red-700">
                    <NuxtLink to="/news" @click="emit('close')">
                        News
                    </NuxtLink>
                </li>
                <li class="hover:underline hover:underline-offset-4 hover:text-red-700">
                    <NuxtLink to="/store" @click="emit('close')">
                        Store
                    </NuxtLink>
                </li>
                <li class="hover:underline hover:underline-offset-4 hover:text-red-700">
                    <NuxtLink to="/contact" @click="emit('close')">
                    Contact
                </NuxtLink>
                </li>
            </ul>
        </div>
    </div>
</template>