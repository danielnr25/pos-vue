<script setup>
    import { RouterLink, useRoute } from 'vue-router'
    import Link from './Link.vue';
    import Logo from './Logo.vue';

  const route = useRoute();
  const isLinkActive = (name) => route.name === name;


</script>


<template>
    <header class="px-10 py-5 bg-gray-900 flex justify-between absolute top-0 w-full z-10">
        <div>
            <Logo />
        </div>

        <nav class="space-x-4">
            <RouterLink
                :to="{name: 'products'}"
                class="rounded text-white font-bold p-2"
                :class="{ 'border-b-2 border-indigo-500 text-indigo-500': isLinkActive('products') }"
            >
                Productos
            </RouterLink>
            <RouterLink
                :to="{name: 'sales'}"
                class="rounded text-white font-bold p-2"
                :class="{ 'border-b-2 border-indigo-500 text-indigo-500': isLinkActive('sales') }"
            >
                Ventas
            </RouterLink>
            <Link
                to="shop"
            >
                Ir a Tienda
            </Link>
        </nav>
    </header>
</template>

