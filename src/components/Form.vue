<template>
    <h1  class="mt-12 text-3xl font-semibold">Test Form</h1>
    <form class="w-80 mx-auto space-y-8" v-on:submit="submitForm($event)">
        <div class="flex flex-col" >
            <label class="text-left">Name</label>
            <input class="border-2 rounded-md p-2 border-gray-500" required name="name"/>
        </div>

        <div class="flex flex-col" >
            <label class="text-left">Email</label>
            <input class="border-2 rounded-md p-2 border-gray-500" required/>
        </div>

        <div class="flex flex-col">
            <label class="text-left">Your Message</label>
            <textarea class="border-2 rounded-md p-2 border-gray-500" required/>
        </div>

        <button class="px-6 py-2 bg-emerald-500 rounded-md text-white" type="submit">Submit</button>
    </form> 
</template>

<script>
    export default {
        name: "Form",
        methods: {
            submitForm: function (event) {
                event.preventDefault()

                alert(`Name: ${event.target.name.value}`)
            }
        }
    }
</script>