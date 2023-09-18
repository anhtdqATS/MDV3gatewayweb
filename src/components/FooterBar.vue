<script setup>
import { containerMaxW } from "@/config.js";
import BaseLevel from "@/components/BaseLevel.vue";
import { useStyleStore } from "@/stores/style";

const styleStore = useStyleStore();
const year = new Date().getFullYear();
</script>

<template>
  <footer
    :class="[
      containerMaxW,
      styleStore.textStyle ? styleStore.textStyle : 'text-gray-500',
    ]"
    class="py-2 px-6"
  >
    <BaseLevel>
      <div class="text-center md:text-left">
        <b>
          <a
            href="https://ats.com.vn"
            target="_blank"
            :class="
              styleStore.textStyle ? styleStore.textStyle : 'text-blue-600'
            "
          >
            ATS JSC &copy; 1998 - {{ year }}
          </a>
        </b>
      </div>
      <ul class="grid grid-cols-4 gap-4">
        <a href="https://ats.com.vn/contact/" target="_blank" class="">
          ATS JSC
        </a>
        <a href="https://ats.com.vn/company-overview/" target="_blank" class=""
          >About Us</a
        >
        <a href="https://www.facebook.com/atsjscvn" target="_blank" class=""
          >Facebook</a
        >
        <a href="#" target="_blank" class="nav-link">License</a>
      </ul>
    </BaseLevel>
  </footer>
</template>
