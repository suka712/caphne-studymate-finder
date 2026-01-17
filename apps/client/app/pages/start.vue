<script setup lang="ts">
definePageMeta({ layout: "internal" })

type Gender = "male" | "female" | "other";
type Vibe = "antara" | "owl" | "quinx";

const currentQuestion = ref(1);
const selectedGender = ref<Gender>();
const selectedVibe = ref<Vibe>();

const totalQuestions = 2;

const next = () => {
  if (currentQuestion.value < totalQuestions) {
    currentQuestion.value++;
  }
}

const previous = () => {
  if (currentQuestion.value > 0) {
    currentQuestion.value--;
  }
}
</script>

<template>
  <div class="flex flex-col justify-center items-center h-screen gap-6">
    <!-- Question 1 -->
    <div v-if="currentQuestion === 1">
      <div class="flex flex-col gap-2 justify-center">
        <div class="flex justify-center gap-2">
          <Button class="hover:px-6" @click="selectedGender = 'male'">Male</Button>
          <Button class="hover:px-6" @click="selectedGender = 'female'">Female</Button>
          <Button variant="outline" class="hover:px-6" @click="selectedGender = 'other'">Other</Button>
        </div>
      </div>
    </div>
    <!-- Question 2 -->
    <div v-if="currentQuestion === 2">
      <div class="flex flex-col gap-2 justify-center">
        <div class="flex justify-center gap-2">
          <Button class="hover:px-6" @click="selectedVibe = 'antara'">Male</Button>
          <Button class="hover:px-6" @click="selectedVibe = 'owl'">Owl</Button>
          <Button class="hover:px-6" @click="selectedVibe = 'quinx'">Quinx</Button>
          <Button variant="outline" class="hover:px-6" @click="selectedGender = 'other'">Other</Button>
        </div>
      </div>
    </div>
    <h1>Your gender is...</h1>
    <div>
      Selected: {{ selectedGender }}
    </div>
  </div>
  <ProgressControl />
</template>