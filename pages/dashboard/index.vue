<template>
    <div class="container">
        <div class="flex flex-col gap-10">
            <div class="home-data flex flex-col gap-5">
                <h1>Current Data</h1>
                <p>Name: athif lanang untoro</p>
                <p>Description: My name is athif lanang untoro, i'm currently in the age of 23 years old, i was born in march 25, 2000 in jakarta, indonesia. i am the first brother of my sister. i currently live in Bumi Serpong Damai, Tangerang Selatan. I have 2 pets, one chihuahua and one corgi.</p>
            </div>
        <div>
            <button type="button" @click="showEdit = !showEdit" class="bg-green-700 text-white px-6 py-2 rounded-lg"
                v-if="!showEdit">Edit</button>
            <button type="button" @click="showEdit = !showEdit" class="bg-green-700 text-white px-6 py-2 rounded-lg"
                v-else>Close</button>
        </div>
            <div :class="showEdit ? 'flex' : 'hidden'" class="edit-form flex-col gap-5">
            <h1>Edit</h1>
                <form class="flex flex-col gap-5 items-start">
                    <div class="input-group w-full">
                        <input type="text" class="border border-green-700 rounded-sm p-2 w-full md:w-1/2"
                        placeholder="Enter new Name">
                    </div>
                    <div class="input-group w-full">
                        <input type="text" class="border border-green-700 rounded-sm p-2 w-full md:w-1/2"
                        placeholder="Enter new Description">
                    </div>
                <button type="button" class="bg-green-700 text-white px-6 py-2 rounded-lg">Edit</button>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
definePageMeta({
    layout: 'dashboard'
})
export default {
    data() {
        return {
            showEdit: false
        }
    }
}
</script>