<script setup>
  const currentTime = ref(new Date().toLocaleTimeString());

  // Функция для прибавления 1 часа
  const addOneHour = () => {
    const date = new Date();
    date.setHours(date.getHours() + 0);
    return date.toLocaleTimeString();
  };

  const intervalId = ref(null);

  onMounted(() => {
    intervalId.value = setInterval(() => {
      currentTime.value = addOneHour(); // Обновляем время с прибавленным 1 часом
    }, 1000);
  });
</script>


<template>
  <div class="">
    <div class="fixed bottom-0 w-full">

      <div class="container mx-auto py-6">

        <div class="flex justify-between items-center">
          
          <div class="flex items-center justify-center py-6">
            <p class="text-white text-2xl">tehnosvar.ru </p>
          </div>

          <div class="">
            <div class="flex w-56 justify-start py-6">
              <p class="text-white text-5xl">{{ currentTime }}</p>
            </div>
          </div>
          
        </div>

      </div>

    </div>
  </div>
</template>