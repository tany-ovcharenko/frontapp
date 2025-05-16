<template>
  <div class="profile">
    <div class="toolbar px-2">
      <UCard>
      <UNavigationMenu
        orientation="horizontal"
        :items="navLinks"
        :ui="{ linkLeadingIcon: 'text-lg square-icon' }"
      />
      <div class="profile-header flex">
            <UButton 
            icon="i-heroicons-user" 
            variant="ghost" 
            color="gray" 
            size="200px"
            class="user"
            aria-label="Toggle theme" 
          />
       
          <div class="profile-details">
                <h1 class="text-lg">Фуфукович Глеб Стопудов<span class="square"></span></h1>
                <p>Кандидат на вакансию: <a href="#" class="link">Жадный благотворитель</a><span class="square"></span> <a href="#" class="link">(14.08.2024 Отклик)</a></p>
                <p>Просмотрено</p>
                <p>Возраст не указан</p>
                <p class="flex items-center"><span class="phone link"></span>+79876543210
                  <a href="#" class="soc whatsapp"></a><a href="#"class="soc viber"></a><a href="#" class="soc telegram"></a>
                </p>
                <p><a href="mailto:test@gmail.com" class="mail">test@gmail.com</a>
                  </p>
                
                
            </div>
           
          </div> 
          Дела:
            <div class="actions">
            <button class="first">Собеседование<br> запланировано</button>
            <button>Создать<br> видеозвонок</button>
            <button>Запланировать<br> событие</button>
            <button>Отправить <br>запрос</button>
        </div>
        Статус рассмотрения:
        
        <div class="status-track">
            <button>Новое</button>
            <button>Просмотрено</button>
            <button>Отправлено приглашение</button>
            <button>Назначено собеседование</button>
            <button>Не дошел</button>
            <button>Проведено собеседование</button>
        </div>
        <div class="footer">
            <p class="font-lg">Pikabu отклик</p>
            <p>Отлик с портала pikabu.</p>
            <br>
            <p><strong>Дата рождения:</strong>1987-04-02</p>
            <p><strong>Гражданство:</strong> Россия</p>
            <br>
            <p>Сопроводительное письмо</p>
            <br>
            <p class="files">Файлы портфолио: <br><span>Резюме:</span></p>
        </div>
        
       
    </UCard>

    </div>

        

    
        

    <div class="card p-4 border ring-default rounded shadow-md">
      <h2 class="card-title text-xl font-bold mb-4">
        Environment Variable Test
      </h2>
      <div class="card-body space-y-2">
        <p>
          <strong>WordPress API URL:</strong>
          <span class="text-blue-500">{{
            config.public.wordpressApiUrl
          }}</span>
        </p>
        <p>
          <strong>API Base URL:</strong>
          <span class="text-blue-500">{{ config.public.apiBase }}</span>
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const config = useRuntimeConfig();

const navLinks = ref([
  {
    to: '/printer',
    icon: 'i-heroicons-printer',
    class: 'square-icon'
  },
  {
    to: '/pdf',
    icon: 'i-heroicons-document',
  },
  {
    to: '/word',
    icon: 'i-heroicons-document-minus',
  },
  {
    to: '/check',
    icon: 'i-heroicons-document-check',
  },
  {
    to: '/box',
    icon: 'i-heroicons-archive-box-x-mark',
  },
  {
    to: '/rectangle',
    icon: 'i-heroicons-arrow-left-end-on-rectangle',
  },
  {
    to: '/heart',
    icon: 'i-heroicons-heart',
  }
]);
onMounted(async () => {
  try {
    const response = await fetch(`https://dev.jobcart.ru/wp-json/test/v2/app`);
    if (!response.ok) {
    throw new Error('Failed to fetch data!!');
    }
    const data = await response.json();
    console.log(data)
    } catch (err) {
    console.error('Error fetching:', err);
    error.value = 'Failed to load items!!';
    }

});
</script>

<style scoped>
.profile {
  padding: 1rem;
}
.toolbar {
  padding: 0.5rem 0;
}
.card-body {
  color: #555;
}
.square-icon {
  width: 1.5em; 
  height: 1.5em; 
  display: inline-flex; 
  align-items: center;
  justify-content: center;
  box-shadow: 0 0 1px 1px #ccc;
}
.user {
    width: 200px !important;
    height: 200px !important;
    border: 1px solid #ccc;
    font-size: 6rem;
    justify-content: center;
    margin-right: 15px;
    margin-bottom: 15px;
}
.actions button {
  width: 150px;
  text-align: center;
  border: 1px solid #326d23;
  background: none;
  margin: 10px 10px 10px 0;
}
.actions .first {
  background: #326d23;
  color: #fff;
}
.status-track {
  display: flex;
  flex-wrap: wrap;
}
.status-track button {
  width: 150px;
  margin: 10px 10px 10px 0;
  background: #a3aebd;
  height: 48px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.font-lg {
  font-size: 20px;
  font-weight: 700;
}
.files {
  background: #43969b;
  color: #fff;
  padding: 20px;
}
.files span {
  color:rgb(35, 70, 174)
}
 

</style>