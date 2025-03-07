<script setup lang="ts">
interface Props {
  title?: string;
  description?: string;
  content?: string;
}

defineProps<Props>();
</script>

<template>
  <Card>
    <CardHeader>
      <CardTitle class="flex items-center">
        {{ title }}
      </CardTitle>
      <CardDescription>
        {{ description }}
      </CardDescription>
    </CardHeader>
    <CardContent>
      <p class="text-slate-700 dark:text-slate-300">
        {{ content }}
      </p>
    </CardContent>
  </Card>
</template>
