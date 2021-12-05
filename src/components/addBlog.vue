<template>
    <div id="add-blog">
        <h2>Add a New Blog Post</h2>
        <form action="">
            <label>Blog Title:</label>
            <input type="text" v-model.lazy="blog.title" required>
            <label>Blog Text:</label>
            <textarea v-model.lazy="blog.content"></textarea>
            <div id="checkboxes">
                <input type="checkbox" value="work" v-model="blog.categories">
                <label>Work</label>
                <input type="checkbox" value="books" v-model="blog.categories">
                <label>Books</label>
                <input type="checkbox" value="movies" v-model="blog.categories">
                <label>Movies</label>
                <input type="checkbox" value="life" v-model="blog.categories">
                <label>Stuff about life</label>
            </div>
        </form>
        <div id="preview">
            <h3>Preview Blog</h3>
            <p>Blog Title: {{ blog.title }}</p>
            <p>Blog Text:</p>
            <p>{{ blog.content }}</p>
            <p>Blog Categories:</p>
            <ul>
                <li v-for="category in blog.categories">{{category}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            blog: {
                title: '',
                content: '',
                categories: []
            }
            
        }
    },
    methods: {

    }
}
</script>

<style scoped>
#add-blog {
    max-width: 480px;
    margin: 30px auto;
}

#add-blog * {
    box-sizing: border-box;
}

label {
    display: block;
    margin: 10px 0;
    width: fit-content;
}

input[type="text"],
textarea {
    width: 100%;
    border-radius: 5px;
    border: 1px solid #ccc;
    font-size: 16px;
    line-height: 1.5;
    padding: 6px 12px;
    display: block;
}

textarea {
    resize: none;
    min-height: 138px;
}

h2 {
    margin: 20px 0;
    text-align: center;
}

h3 {
    margin: 16px 0;
    text-align: center;
}

#preview {
    border: 1px solid #ccc;
    padding: 8px;
}

#checkboxes {
    padding: 10px 0;
}

#checkboxes input {
    display: inline-block;
    margin-right: 6px;
}

#checkboxes label {
    display: inline-block;
    margin-right: 10px;
}
</style>