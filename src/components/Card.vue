<script lang="ts">

export default {
    props: {
        lg: Boolean,
        title: String,
        icon: String,
        body: String,
        url: String
    }
}

</script>

<template>
    <div v-if="lg" class="bg-white rounded-lg shadow-md p-5 col-span-2">
        <div class="flex justify-start items-center">
            <h1 class="font-semibold text-xl mr-2">{{ title }}</h1>
            <img v-bind:src="icon" class="h-8 w-auto" />
        </div>
        <p class="font-light text-ms w-full text-gray-500">{{ body }}</p>
        <div class="flex mt-3 justify-end items-center">
            <a v-bind:href="url" target="_blank" class="font-light text-sm text-blue-500 underline">
                Learn More
            </a>
        </div>
    </div>
    <div v-if="!lg" class="bg-white rounded-lg shadow-md p-5 col-span-1">
        <div class="flex justify-start items-center">
            <h1 class="font-semibold text-xl mr-2">{{ title }}</h1>
            <img v-bind:src="icon" class="h-8 w-auto" />
        </div>
        <p class="font-light text-ms text-gray-500 w-90">{{ body }}</p>
        <div class="flex mt-3 justify-end items-center">
            <a v-bind:href="url" target="_blank" class="font-light text-sm text-blue-500 underline">
                Learn More
            </a>
        </div>
    </div>
</template>