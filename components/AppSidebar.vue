<script setup lang="ts">
import {
  Calendar,
  Home,
  Inbox,
  Search,
  Settings,
  PanelLeftOpen,
  PanelLeftClose,
} from "lucide-vue-next";
import { ref, watch } from "vue";

const isCollapsed = ref(false);
const sidebarWidth = ref(isCollapsed.value ? "64px" : "240px");

// Menu items.
const items = [
  {
    title: "Home",
    url: "/",
    icon: Home,
  },
  {
    title: "Vista 2",
    url: "/vista2",
    icon: Inbox,
  },
  {
    title: "Vista 3",
    url: "/vista3",
    icon: Calendar,
  },
  {
    title: "Search",
    url: "#",
    icon: Search,
  },
  {
    title: "Settings",
    url: "#",
    icon: Settings,
  },
];

// Watch for changes in isCollapsed
watch(isCollapsed, (newValue) => {
  sidebarWidth.value = newValue ? "64px" : "240px";
});
</script>

<template>
  <aside
    class="h-screen bg-white border-r transition-all duration-300 relative"
    :style="{ width: sidebarWidth }"
  >
    <Button
      size="small"
      @click="isCollapsed = !isCollapsed"
      class="absolute -right-3 top-6 z-50 bg-white p-1 border shadow-sm hover:bg-gray-100"
    >
      <PanelLeftOpen v-if="!isCollapsed" class="h-4 w-4 text-black" />
      <PanelLeftClose v-else class="h-4 w-4 text-black" />
    </Button>

    <div class="h-full overflow-y-auto">
      <div class="p-4">
        <h2 class="font-semibold mb-4" v-if="!isCollapsed">Application</h2>
        <nav>
          <ul class="space-y-2">
            <li v-for="item in items" :key="item.title">
              <NuxtLink
                :to="item.url"
                class="flex items-center gap-2 p-2 rounded-lg hover:bg-gray-100"
                :class="{ 'justify-center': isCollapsed }"
              >
                <component :is="item.icon" class="h-5 w-5" />
                <span v-if="!isCollapsed">{{ item.title }}</span>
              </NuxtLink>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </aside>
</template>

<style scoped>
aside {
  min-width: v-bind(sidebarWidth);
}
</style>
