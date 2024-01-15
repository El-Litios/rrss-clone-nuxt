<template>
  <div class="h-screen flex flex-col">
    <div
      class="p-2 my-2 rounded-full hover:bg-blue-50 w-min dark:hover:bg-white/20"
      :class="defaultTransition"
    >
      <NuxtLink to="/">
        <div class="w-8 h-8">
          <LogoTwitter />
        </div>
      </NuxtLink>
    </div>

    <div class="mt-2 space-y-3">
      <SideBarLeftTab v-for="item in sidebarItems" :key="item.name" active>
        <template v-slot:icon>
          <component :is="item.icon" />
        </template>
        <template v-slot:name>{{ item.name }}</template>
      </SideBarLeftTab>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { HomeIcon } from "@heroicons/vue/solid";
import {
  HashtagIcon,
  BellIcon,
  InboxIcon,
  BookmarkIcon,
  DocumentTextIcon,
  UserIcon,
  DotsCircleHorizontalIcon,
} from "@heroicons/vue/outline";

const defaultTransition = useTailwindConfig();

const sidebarItems = [
  { name: "Home", icon: HomeIcon },
  { name: "Explore", icon: HashtagIcon },
  { name: "Notifications", icon: BellIcon },
  { name: "Messages", icon: InboxIcon },
  { name: "Bookmarks", icon: BookmarkIcon },
  { name: "Documents", icon: DocumentTextIcon },
  { name: "User", icon: UserIcon },
  { name: "More", icon: DotsCircleHorizontalIcon },
];
</script>
