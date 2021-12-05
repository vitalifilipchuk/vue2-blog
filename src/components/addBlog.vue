<template>
    <div id="add-blog">
        <h2>Add a New Blog Post</h2>
        <form action="">
            <label>Blog Title:</label>
            <input type="text" required>
            <label>Blog Text:</label>
            <textarea></textarea>
        </form>
        <div id="preview">
            <h3>Preview Blog</h3>
            <p>Blog Title:</p>
            <p>Blog Text:</p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {

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
    text-align: left;
    margin: 10px 0;
}

input[type="text"],
textarea {
    width: 100%;
    border-radius: 5px;
    border: 1px solid #333;
    font-size: 16px;
    line-height: 1.5;
    padding: 6px 12px;
}

textarea {
    resize: none;
    min-height: 138px;
}
</style>