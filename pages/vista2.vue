<script setup lang="ts">
import Autoplay from "embla-carousel-autoplay";

const carouselImages = [
  "/images/1.jpg",
  "/images/3.jpg",
  "/images/4.jpg",
  "/images/5.jpg",
];
</script>

<template>
  <ScrollArea className="h-full bg-slate-50 dark:bg-slate-950">
    <div class="p-6">
      <div class="max-w-7xl mx-auto">
        <header class="mb-10">
          <h1 class="text-3xl font-bold text-gray-900 dark:text-white mb-4">
            Recursos y Enlaces
          </h1>
          <p class="text-gray-600 dark:text-gray-300">
            Explora nuestra colección de recursos sobre ciberseguridad y defensa
            nacional
          </p>
        </header>

        <div class="mb-12 relative">
          <Carousel
            class="w-[calc(100%-2rem)] mx-auto rounded-xl overflow-hidden shadow-lg"
            :opts="{
              align: 'center',
              loop: true,
            }"
            :plugins="[
              Autoplay({
                delay: 4000,
              }),
            ]"
          >
            <CarouselContent>
              <CarouselItem
                v-for="(image, index) in carouselImages"
                :key="index"
                class="pl-1 basis-full"
              >
                <Card class="border-0">
                  <CardContent class="p-0">
                    <div class="relative aspect-video">
                      <img
                        :src="image"
                        :alt="`Slide ${index + 1}`"
                        class="w-full h-full object-cover"
                      />
                    </div>
                  </CardContent>
                </Card>
              </CarouselItem>
            </CarouselContent>
            <CarouselPrevious class="left-4" />
            <CarouselNext class="right-4" />
          </Carousel>
        </div>

        <div class="flex justify-center">
          <Card class="w-[800px] shadow-lg transition-shadow hover:shadow-xl">
            <CardHeader>
              <CardTitle>Enlaces Útiles</CardTitle>
              <CardDescription>
                Recursos e información relevante sobre ciberseguridad y defensa
              </CardDescription>
            </CardHeader>
            <CardContent class="py-4">
              <ul class="space-y-2">
                <li>
                  <NuxtLink
                    to="https://www.cvi.icrt.cu/compromiso-con-la-defensa-diaz-canel-y-estudiantes-de-la-uci-en-accion/"
                    target="_blank"
                    class="text-blue-600 hover:text-blue-800 dark:text-blue-400 dark:hover:text-blue-300"
                  >
                    Compromiso con la Defensa - UCI
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink
                    to="https://www.uci.cu/"
                    target="_blank"
                    class="text-blue-600 hover:text-blue-800 dark:text-blue-400 dark:hover:text-blue-300"
                  >
                    Universidad de las Ciencias Informáticas
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink
                    to="https://www.tribuna.cu/cuba/2025-01-30/para-cuba-la-ciberseguridad-es-una-prioridad"
                    target="_blank"
                    class="text-blue-600 hover:text-blue-800 dark:text-blue-400 dark:hover:text-blue-300"
                  >
                    La Ciberseguridad es una Prioridad
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink
                    to="https://www.cipi.cu/la-ciberseguridad-el-ciberespacio-internet-y-las-tecnologias-de-la-informacion-y-las-comunicaciones/"
                    target="_blank"
                    class="text-blue-600 hover:text-blue-800 dark:text-blue-400 dark:hover:text-blue-300"
                  >
                    Ciberseguridad y Tecnologías de la Información
                  </NuxtLink>
                </li>
              </ul>
            </CardContent>
          </Card>
        </div>
      </div>
    </div>
  </ScrollArea>
</template>

<style scoped>
.carousel-container {
  margin-left: calc(var(--sidebar-width) + 2rem);
}
</style>
