<template>
  <div>
    <div class="container">
      <UCard>
        <div class="toolbar profile">
          <div class="profile-menu flex mb-3">
            <a href="#" class="printer-icon mr-3"></a>
            <a href="#" class="pdf-icon mr-3"></a>
            <a href="#" class="doc-icon mr-3"></a>
            <a href="#" class="list-icon mr-3"></a>
            <a href="#" class="basket-icon mr-3"></a>
            <a href="#" class="send-icon mr-3"></a>
            <a href="#" class="favor-icon"></a>
          </div>
        </div>
        <div class="profile-header flex">
            <div class="profile-image mr-3">
            </div>
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

        <div class="actions">
            <button>Собеседование запланировано</button>
            <button>Создать видеозвонок</button>
            <button>Запланировать событие</button>
            <button>Отправить запрос</button>
        </div>

        <div class="status-track">
            <button>Новое</button>
            <button>Просмотрено</button>
            <button>Отправлено приглашение</button>
            <button>Назначено собеседование</button>
            <button>Не дошел</button>
            <button>Проведено собеседование</button>
        </div>

        <div class="footer">
            <p>Pikabu отклик</p>
            <p>Отлик с портала pikabu.</p>
            <p>Дата рождения: 1987-04-02</p>
            <p>Гражданство: Россия</p>
            <p>Сопроводительное письмо</p>
            <p>Файлы портфолио: Резюме:</p>
        </div>
      </UCard>
    </div>
 
    
    <!-- Тестовый компонент для проверки переменных окружения -->
    <EnvTest class="mb-6" />
    
    <div class="flex items-center my-6">
      <div class="h-px bg-gray-200 dark:bg-gray-700 flex-grow"></div>
      <span class="px-3 text-sm text-gray-500 dark:text-gray-400">Demo Content</span>
      <div class="h-px bg-gray-200 dark:bg-gray-700 flex-grow"></div>
    </div>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-6">
      <UCard>
        <template #header>
          <h3 class="text-lg font-semibold">Sidebar Features</h3>
        </template>
        <ul class="list-disc pl-5 space-y-2">
          <li>Responsive design</li>
          <li>Collapsible sidebar</li>
          <li>WordPress API integration</li>
          <li>Dark/Light mode toggle</li>
        </ul>
      </UCard>
      
      <UCard>
        <template #header>
          <h3 class="text-lg font-semibold">Nuxt UI Components</h3>
        </template>
        <ul class="list-disc pl-5 space-y-2">
          <li>Custom sidebar with responsive design</li>
          <li>UCards for content display</li>
          <li>UButtons for actions</li>
          <li>UIcon for menu icons</li>
        </ul>
      </UCard>
    </div>
  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'default'
});
</script> 