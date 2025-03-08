<script setup lang="ts">
import { ref } from "vue";
import { DatePicker as DatePickerOrigin } from "vant";
import { DatePicker } from "./components/date-picker";
import "vant/es/date-picker/style";

const minDateOrigin = new Date(2025, 2, 10);
const maxDateOrigin = new Date(2025, 3, 30);
const dateOrigin = ref(["2025", "04", "01"]);
const handleConfirmOrigin = ({
  selectedIndexes,
  selectedOptions,
  selectedValues,
}) => {
  console.log("[origin]selectedValues :>> ", selectedValues);
};

const minDate = new Date(2025, 2, 10);
const maxDate = new Date(2025, 3, 30);
const date = ref(["2025", "04", "01"]);
const handleConfirm = ({
  selectedIndexes,
  selectedOptions,
  selectedValues,
}) => {
  console.log("selectedValues :>> ", selectedValues);
};
</script>

<template>
  <div class="container">
    <div class="card">
      <DatePickerOrigin
        title="[origin]日期选择器"
        v-model="dateOrigin"
        :min-date="minDateOrigin"
        :max-date="maxDateOrigin"
        @confirm="handleConfirmOrigin"
      />
    </div>

    <div class="card">
      <DatePicker
        title="日期选择器"
        v-model="date"
        :min-date="minDate"
        :max-date="maxDate"
        @confirm="handleConfirm"
      />
    </div>
  </div>
</template>

<style scoped>
.container {
  padding: 12px 0;
  margin: 0 12px;
  display: flex;
  row-gap: 12px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  box-sizing: border-box;
}
.card {
  flex: 1;
  border: 1px solid #ccc;
  width: 100%;
}
</style>
