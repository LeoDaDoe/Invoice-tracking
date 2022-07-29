<template>
    <Bar :chart-options="chartOptions" :chart-data="chartData" :chart-id="chartID" :dataset-id-key="datasetIdKey"
        :plugins="plugins" :css-classes="cssClasses" :styles="styles" :width="chartWidth" :height="chartHeight" />
</template>

<script lang="ts">
import { defineComponent, h, PropType } from "vue";
import { Bar } from 'vue-chartjs/legacy'
import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    BarElement,
    CategoryScale,
    LinearScale,
    PluginOptionsByType,
} from "chart.js";

ChartJS.register(
    Title,
    Tooltip,
    Legend,
    BarElement,
    CategoryScale,
    LinearScale
);

export default defineComponent({
    name: "WorkHourGraph",
    components: { Bar },
    props: {
        chartID: {
            type: String,
            defaults: "bar-chart",
        },
        chartWidth: {
            type: Number,
            default: 400,
        },
        chartHeight: {
            type: Number,
            default: 1100,
        },
        datasetIdKey: {
            type: String,
            default: 'label'
        },
        cssClasses: {
            type: String,
            default: "",
        },
        styles: {
            type: Object as PropType<Partial<CSSStyleDeclaration>>,
            // eslint-disable-next-line
            default: () => { },
        },
        plugins: {
            type: Array,
            default: () => [],
        },
    },
    data() {
        return {
            chartData: {
                labels: ['January', 'February', 'March'],
                datasets: [{ data: [40, 20, 12] }]
            },
            chartOptions: {
                responsive: true,
                maintainAspectRatio: false
            }
        }
    }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
