<template>
  <SidebarProvider>
    <div class="flex h-screen">
      <AppSidebar />
      <main class="flex-1 p-4">
        <slot />
      </main>
    </div>
  </SidebarProvider>
</template>
