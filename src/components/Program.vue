<script setup>
import { ref } from "vue";

const day = ref(1);

const tableData = ref({
  1: {
    title: "Main Hall",
    data: [
      { id: 1, time: "08.30 – 09.45", title: "Registration", description: "" },
      { id: 2, time: "09.00 – 09.45", title: "Business coffee", description: "" },
      { id: 3, time: "10.00 – 10.15", title: "Official opening of the forum:", description: "Khudayarov A.A., Minister of Health" },
      {
        id: 4,
        time: "10.15 - 12.00",
        title: "Plenary session",
        description: "Adaptation and development of the pharmaceutical industry to today's realities.",
      },
      {
        id: 5,
        time: "12.00 – 13.30",
        title: "Panel session 1",
        description: "Transformation of the drug supply system process: from challenges to solutions.",
      },
      { id: 6, time: "13.30 - 14.30", title: "Lunch at the restaurant", description: "" },
      { id: 7, time: "16.00 – 16.30", title: "Сoffee break", description: "" },
      { id: 8, time: "09.00 – 09.45", title: "Business coffee", description: "" },
      { id: 9, time: "10.00 – 10.15", title: "Official opening of the forum:", description: "Khudayarov A.A., Minister of Health" },
      {
        id: 10,
        time: "10.15 - 12.00",
        title: "Plenary session",
        description:
          "Adaptation and development of the pharmaceutical industry to today's realities. Development of the pharmaceutical industry",
      },
      { id: 11, time: "10.00 – 10.15", title: "Official opening of the forum:", description: "Khudayarov A.A., Minister of Health" },
      {
        id: 12,
        time: "10.15 - 12.00",
        title: "Plenary session",
        description:
          "Adaptation and development of the pharmaceutical industry to today's realities. Development of the pharmaceutical industry",
      },
    ],
  },
  2: {
    title: "Main Hall",
    data: [
      {
        id: 1,
        time: "10.00 – 11.30",
        title: "Panel session 4",
        description:
          "Current strategies of the pharmaceutical market in  Eurasia. View of the largest market players. Growth drivers, challenges and prospects",
      },
      { id: 2, time: "11.30 – 12.00", title: "Coffee break", description: "" },
      {
        id: 3,
        time: "12.00 – 13.30",
        title: "Panel session 5",
        description: "Pharmaceutical safety and quality: global standards and practices.",
      },
      {
        id: 4,
        time: "13.30 – 14.30",
        title: "Lunch at the restaurant",
        description: "Adaptation and development of the pharmaceutical industry to today's realities.",
      },
      {
        id: 5,
        time: "14.30 – 16.00",
        title: "Panel session 6",
        description: "New era of pharmaceutical distribution in Uzbekistan: challenges and solutions.",
      },
      { id: 6, time: "11.30 – 12.00", title: "Coffee break", description: "" },
      {
        id: 7,
        time: "12.00 – 13.30",
        title: "Panel session 5",
        description: "Pharmaceutical safety and quality: global standards and practices.",
      },
      {
        id: 8,
        time: "13.30 – 14.30",
        title: "Lunch at the restaurant",
        description: "Adaptation and development of the pharmaceutical industry to today's realities.",
      },
      { id: 9, time: "11.30 – 12.00", title: "Coffee break", description: "" },
    ],
  },
});

function getDayValue(val) {
  day.value = val;
}
</script>

<template>
  <div style="background-color: #ffffff" class="hero_area">
    <svg
      class="waves"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      viewBox="0 24 150 28"
      preserveAspectRatio="none"
      shape-rendering="auto">
      <defs><path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"></path></defs>
      <g class="parallax">
        <use xlink:href="#gentle-wave" x="48" y="0" fill="#C1EDE2"></use>
        <use xlink:href="#gentle-wave" x="48" y="3" fill="#059A77"></use>
      </g>
    </svg>
  </div>

  <div class="program">
    <div class="container">
      <div class="header flex flex-col">
        <h2>Program</h2>
        <p>The final version of the forum program will be available soon</p>
      </div>
      <div class="content-tabs">
        <div class="tabs">
          <div class="border"></div>
          <div class="buttons">
            <div class="flex gap-2">
              <div>
                <button
                  type="button"
                  @click="getDayValue(1)"
                  class="bg-transparent border-green"
                  :class="{ 'bg-light-green border-0': day == 1 }">
                  <div>DAY 1</div>
                </button>
              </div>
              <div>
                <button
                  type="button"
                  @click="getDayValue(2)"
                  class="bg-transparent border-green"
                  :class="{ 'bg-light-green border-0': day == 2 }">
                  <div>DAY 2</div>
                </button>
              </div>
            </div>
          </div>
          <div class="border"></div>
        </div>
      </div>

      <div class="time-table">
        <table class="text-white">
          <tr>
            <th></th>
            <th>{{ tableData[day].title }}</th>
          </tr>
          <template v-for="item in tableData[day].data" :key="item.id">
            <tr>
              <td>
                <span class="time">{{ item.time }}</span>
              </td>
              <td>
                <h5 class="title">{{ item.title }}</h5>
              </td>
            </tr>
            <tr>
              <td></td>
              <td>
                <span class="description">{{ item.description }}</span>
              </td>
            </tr>
          </template>
        </table>
      </div>

      <div class="table-content text-white">
        <h2 class="my-3">{{ tableData[day].title }}</h2>
        <div class="flex flex-col gap-5">
          <template v-for="item in tableData[day].data" :key="item.id">
            <div>
              <div class="time">{{ item.time }}</div>
              <div class="title">{{ item.title }}</div>
              <div class="description">{{ item.description }}</div>
            </div>
          </template>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>

.table-content {
  margin: 10px;
  display: none;
}
.table-content h2 {
  text-align: center;
  font-size: 28px;
  line-height: 150%;
}
.table-content .time,
.table-content .title,
.table-content .description {
  font-size: 22px;
  line-height: 150%;
  margin: 5px 0;
}
.table-content .description {
  opacity: 0.8;
}
.program {
  padding: 160px 0;
  background: #059a77;
}
.header {
  gap: 32px;
  margin-bottom: 32px;
}
.header h2 {
  color: #fff;
  font-size: 48px;
  line-height: 150%;
  text-align: center;
}
.header p {
  text-align: center;
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  color: #fff;
  opacity: 0.8;
}

.tabs {
  align-items: center;
  display: flex;
  justify-content: center;
  position: relative;
}
.tabs .border {
  border-top: 1px dashed rgba(255, 255, 255, 0.4);
  flex-grow: 1;
  height: 1px;
}
.tabs .buttons {
  padding: 0 8px;
  z-index: 9;
}
.tabs .buttons button {
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  font-size: 20px;
  gap: 8px;
  line-height: 150%;
  color: #fff;
  font-weight: 600;
}
.time-table {
  width: 75%;
  margin-bottom: 32px;
  margin: 20px auto;
}
.time-table th {
  font-size: 28px;
  line-height: 150%;
}
table tr th:first-child {
  display: flex;
  padding-right: 12px;
}
table tr td:first-child,
table tr th:first-child {
  display: flex;
  padding-right: 12px;
}
table tr td,
table tr th {
  padding: 5px 12px;
}
table tr th {
  text-align: left;
}
td .time {
  text-wrap: nowrap;
  font-size: 22px;
  line-height: 150%;
}
td .title {
  text-wrap: nowrap;
  font-size: 22px;
  line-height: 150%;
  font-weight: 600;
}
td .description {
  font-size: 22px;
  line-height: 150%;
  opacity: 0.8;
}

marquee {
  margin-bottom: -10px;
}

@media (max-width: 1000px) {
  .program {
    padding: 80px 0;
  }
  .time-table {
    width: 100%;
  }
}
@media (max-width: 576px) {
  .header h2 {
    font-size: 34px;
  }
  .header p {
    text-align: start;
  }
  .tabs .buttons button {
    border-radius: 15px;
    padding: 13px 20px;
    font-size: 16px;
    line-height: 80%;
  }
  .table-content {
    display: block;
  }
  .time-table {
    display: none;
  }
}
</style>
