<template>
    <div class="work-hour-view">
        <b-row cols="10">
            <b-col  cols="3">
                <!-- <div class="row mh-100  mw-100" style="height:100%"> -->
                <b-button class="mt-3">Add new entry</b-button>
                <b-table :sticky-header="tableHeight" :responsive="true" striped hover :items="workEntries"
                    :fields="tableFields" :stickyColumn="true" class="mt-3">
                    <template v-slot:cell(delete)="{ item }">
                        <span>
                            <b-btn @click="testLog(item.message)">Delete</b-btn>
                        </span>
                    </template>
                </b-table>
            <div style="border-style:solid; border-width:W 2px; border-radius: 5px; height:200px"></div>
            </b-col>

            <b-col cols="7">
                <div >
                    <WorkHourGraph />
                </div>
            </b-col>
            <!-- </div> -->
        </b-row>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import WorkHourGraph from "../components/WorkHoursComponents/WorkHourGraph.vue";

interface tableRow {
    date: string,
    message: string
}

export default defineComponent({
    name: 'WorkHoursView',
    props: {
        tableHeight: {
            type: String,
            default: '800px'

        }
    },
    methods: {
        testLog(workEntries: tableRow) {
            console.log(workEntries)
        }
    },
    components: {
        WorkHourGraph
    },
    data() {
        return {
            tableFields: ['date', 'message', 'delete'],
            workEntries: [
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-24', message: 'eReq' },
                { date: '2022-07-25', message: 'OEM' }
            ]
        }
    }
})

</script>
