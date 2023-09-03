<template>
    <div class="app">
        <form>
            <h5>Создание поста</h5>
            <input class="form-input" type="text" placeholder="Название">
            <input class="form-input" type="text" placeholder="Описание">
            <button @click="addPost">Добавить</button>
        </form>
        <div class="posts">
            <div class="post" v-for="post in posts">
                <div><strong>Название:</strong>{{ post.name }}</div>
                <div><strong>Описание:</strong>{{ post.description }}</div>
                <div><strong>Лайки:</strong>{{ post.likes }}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            posts: [
                {
                    id: 1,
                    name: 'Post 1',
                    description: 'Описание поста 1',
                    likes: 1
                },
                {
                    id: 2,
                    name: 'Post 2',
                    description: 'Описание поста 2',
                    likes: 0
                }
            ]
        }
    },
    methods: {
        addPost() {
            this.posts.push({ id: 4, name: 'Push', description: 'Desc', likes: 2 })
        },
        removePost() {
            this.post = [...this.post.pop()]
        }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.posts {
    padding: 1rem;
}

.post {
    padding: 1rem;
    border: 2px solid grey;
    margin-bottom: 1rem;
}

.form-input {
    width: 100%;
    padding: 10px 15px;
    border: 1px solid silver;
    margin-bottom: 1rem;
}

.app {
    padding: 1rem;
}
</style>