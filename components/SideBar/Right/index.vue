<template>
  <div class="flex flex-col">
    <!-- Preview Card "What's happening"-->
    <SideBarRightPreviewCard title="What's happening">
      <SideBarRightPreviewCardItem v-for="items in whatHappeningItems">
        <div>
          <h2 class="font-bold text-gray-800 text-md dark:text-white">
            {{ items.title }}
          </h2>
          <p class="text-xs text-gray-400">
            {{ items.count }}
          </p>
        </div>
      </SideBarRightPreviewCardItem>
    </SideBarRightPreviewCard>

    <!-- Preview Card "Who to follow"-->
    <SideBarRightPreviewCard title="Who to follow">
      <SideBarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems">
        <div class="flex flex-row items-center justify-between p-2">
          <div class="flex flex-row">
            <img
              class="w-10 h-10 rounded-full"
              :src="whoToFollow.avatar"
              :alt="whoToFollow.name"
            />

            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">
                {{ whoToFollow.name }}
              </h1>
              <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button
              class="px-4 py-2 text-xs font-bold text-white bg-black rounded-full dark:text-black dark:bg-white"
            >
              Follow
            </button>
          </div>
        </div>
      </SideBarRightPreviewCardItem>
    </SideBarRightPreviewCard>
  </div>
</template>

<script lang="ts" setup>
const whatHappeningItems = ref([
  {
    title: "#SpaceX",
    count: "19.9k tweets",
  },
  {
    title: "#SpaceX",
    count: "19.9k tweets",
  },
  {
    title: "#SpaceX",
    count: "19.9k tweets",
  },
]);

const whoToFollowItems = ref([
  {
    name: "John Doe",
    handle: "@johndoe",
    avatar: "https://picsum.photos/200/200",
  },
]);
</script>
