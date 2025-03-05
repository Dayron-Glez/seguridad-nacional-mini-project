<template>
  <SidebarProvider>
    <div class="flex min-h-screen">
      <AppSidebar />
      <main class="flex-1 p-4">
        <slot />
      </main>
    </div>
  </SidebarProvider>
</template>
