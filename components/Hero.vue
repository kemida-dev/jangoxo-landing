<template>
  <div
    class="flex flex-col gap-12 my-10 lg:items-center lg:flex-row min-h-[400px] sm:min-h-[700px]"
  >
    <div class="flex-1 w-full">
      <div class="overflow-hidden flex items-center justify-center my-8">
        <div
          class="flex items-center justify-center bg-blue-400 p-2 px-3 rounded-lg text-white"
        >
          <Icon class="w-5 h-5" name="lucide:star" />
          <span class="ml-2 text-sm pt-px font-semibold">Aplicación en Desarrollo</span>
        </div>
      </div>
      <h1 class="text-4xl font-bold text-zinc-800 sm:text-8xl text-balance text-center">
        Transforma tu Cocina en un
        <span class="text-blue-500">Centro de Excelencia</span>
      </h1>
      <p class="max-w-xl sm:max-w-4xl mt-4 text-zinc-600 text-2xl text-center mx-auto">
        Optimiza la organización de tu cocina y gestiona tu inventario con nuestra
        solución integral diseñada específicamente para restaurantes modernos.
      </p>
      <div class="flex flex-wrap gap-4 my-12 items-center justify-center">
        <NuxtLink
          class="inline-flex px-6 py-3 text-lg text-white duration-300 bg-blue-500 rounded-sm hover:opacity-80 cursor-pointer transition-color items-center"
        >
          Solicitar demo gratuita
          <Icon class="w-5 h-5 ml-2" name="lucide:arrow-right" />
        </NuxtLink>
        <NuxtLink
          class="inline-flex px-6 py-3 text-lg hover:text-white duration-300 rounded-sm border shadow-sm items-center cursor-pointer hover:opacity-70 transition-color hover:bg-blue-400 hover:border-transparent"
        >
          Ver Características
        </NuxtLink>
      </div>
      <div class="flex justify-center gap-8">
        <span class="flex items-center gap-1 text-zinc-500">
          <Icon class="w-5 h-5 ml-2 text-blue-500 fill-current" name="lucide:circle-small" />
          <span class="text-sm pt-[2px]"> Sin instalación compleja </span>
        </span>
        <span class="flex items-center gap-1 text-zinc-500">
          <Icon class="w-5 h-5 ml-2 text-blue-500 fill-current" name="lucide:circle-small" />
          <span class="text-sm pt-[2px]"> Soporte 24/7 </span>
        </span>
        <span class="flex items-center gap-1 text-zinc-500">
          <Icon class="w-5 h-5 ml-2 text-blue-500 fill-current" name="lucide:circle-small" />
          <span class="text-sm pt-[2px]"> Resultados inmediatos </span>
        </span>
      </div>
    </div>
  </div>
</template>
