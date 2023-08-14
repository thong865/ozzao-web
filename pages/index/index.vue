<template>
  <div>
    <div class="grid grid-cols-5 gap-3">
        <ProductCardList v-for="i in 20" :key="i"/>
    </div>
    
  </div>
</template>