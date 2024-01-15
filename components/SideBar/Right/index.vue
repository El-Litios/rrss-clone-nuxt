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
      <SideBarRightPreviewCardItem v-for="items in whoToFollowItems">
        <div class="flex flex-row justify-between p-2">
          <div class="flex flex-row">
            <img class="w-10 h-10 rounded-full" src="" alt="aaa">
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
    count: "19.9k tweets",
  },
]);
</script>
