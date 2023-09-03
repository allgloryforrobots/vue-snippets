<template>
    <div>
        <div>
            <button @click="addLike">Likes</button>
            <button @click="addDislike">Dislikes</button>
            <button @click="removeLike">Rm Likes</button>
            <button @click="removeDislike">Rm Dislikes</button>
        </div>
        <div>Количество лайков <strong>{{ likes }}</strong></div>
        <div>Количество дизлайков <strong>{{ dislikes }}</strong></div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                likes: 0,
                dislikes: 0
            }
        },
        methods: {
            addLike() {
                this.likes += 1
            },
            addDislike() {
                this.dislikes += 1
            },
            removeLike() {
                this.likes -= 1
            },
            removeDislike() {
                this.dislikes -= 1
            }
        }
    }
</script>

<style>

</style>