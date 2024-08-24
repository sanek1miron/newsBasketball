<template>
    <div class="comments-section">
      <h3>Комментарии ({{ comments.length }})</h3>
      
      <!-- Форма добавления комментария -->
      <div class="comment-form">
        <input 
          v-model="newComment.name" 
          type="text" 
          placeholder="Ваше имя" 
        />
        <textarea 
          v-model="newComment.text" 
          placeholder="Ваш комментарий">
        </textarea>
        <button @click="addComment">Отправить комментарий</button>
      </div>
  
      <!-- Отображение комментариев -->
      <div class="comments-list">
        <div 
          v-for="(comment, index) in comments" 
          :key="index" 
          class="comment"
        >
          <strong>{{ comment.name }}</strong>
          <p>{{ comment.text }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        comments: [], // Список комментариев
        newComment: {
          name: '',
          text: ''
        } // Объект для нового комментария
      };
    },
    methods: {
      addComment() {
        if (this.newComment.name && this.newComment.text) {
          this.comments.push({ 
            name: this.newComment.name, 
            text: this.newComment.text 
          });
          // Очищаем поля формы после добавления комментария
          this.newComment.name = '';
          this.newComment.text = '';
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .comments-section {
    margin-top: 30px;
  }
  
  .comment-form {
    margin-bottom: 20px;
  }
  
  .comment-form input,
  .comment-form textarea {
    width: 100%;
    padding: 10px;
    margin-bottom: 10px;
    border-radius: 4px;
    border: 1px solid #ccc;
  }
  
  .comment-form button {
    background: rgb(209, 49, 49);
    color: #ffffff;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .comment-form button:hover {
    background: rgb(78, 175, 14);
  }
  
  .comments-list .comment {
    margin-bottom: 20px;
    padding: 10px;
    border-radius: 4px;
    background: #011222;
    color: #fafafa;
    background: #da9203;
    
  }
  
  .comments-list .comment strong {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    
  }
  
  .comments-list .comment p {
    margin: 0;
  }
  </style>
  