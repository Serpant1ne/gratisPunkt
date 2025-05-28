<template>
  <Header />
  <Map class="z-0" />
  <NuxtPage />
  <ScnButton
    size="lg"
    ref="listButton"
    @click="openDrawer"
    class="absolute left-1/2 -translate-x-1/2 bottom-12 z-10 w-fit rounded-full font-semibold items-center text-lg">
    <List :stroke-width="2.5" /> List View
  </ScnButton>
  <ScnDrawer class="z-50">
    <ScnDrawerTrigger ref="drawerTriggerButton" class="hidden">
      Open
    </ScnDrawerTrigger>
    <ScnDrawerContent class="z-50">
      <ScnDrawerHeader>
        <ScnDrawerTitle>Are you absolutely sure?</ScnDrawerTitle>
        <ScnDrawerDescription>
          This action cannot be undone.
        </ScnDrawerDescription>
      </ScnDrawerHeader>
      <ScnDrawerFooter>
        <ScnButton>Submit</ScnButton>
        <ScnDrawerClose>
          <ScnButton variant="outline"> Cancel </ScnButton>
        </ScnDrawerClose>
      </ScnDrawerFooter>
    </ScnDrawerContent>
  </ScnDrawer>
</template>

<script lang="ts" setup>
import { List } from "lucide-vue-next";

const listButton = ref();
const drawerTriggerButton = ref();

function openDrawer() {
  console.log("triggered");
  // For custom components, access the DOM element via $el
  const trigger = drawerTriggerButton.value;
  if (!trigger) return;
  // Try to click the underlying element
  console.log("pass");
  if (trigger.$el) {
    trigger.$el.click();
  } else if (typeof trigger.click === "function") {
    trigger.click();
  } else {
    console.warn("Cannot find DOM element to click");
  }
}
</script>
