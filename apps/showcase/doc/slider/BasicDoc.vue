<template>
    <DocSectionText v-bind="$attrs">
        <p>Slider is used with the <i>v-model</i> property for two-way value binding.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <Slider v-model="value" class="w-56" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script>
export default {
    data() {
        return {
            value: null,
            code: {
                basic: `
<Slider v-model="value" class="w-56" />
`,
                options: `
<template>
    <div class="card flex justify-center">
        <Slider v-model="value" class="w-56" />
    </div>
</template>

<script>
export default {
    data() {
        return {
            value: null
        }
    }
};
<\/script>
`,
                composition: `
<template>
    <div class="card flex justify-center">
        <Slider v-model="value" class="w-56" />
    </div>
</template>

<script setup>
import { ref } from 'vue';

const value = ref(null);
<\/script>
`
            }
        };
    }
};
</script>
