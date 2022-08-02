<template>
    <div>
        <button>deselect rows</button>
        <ag-grid-vue class="ag-theme-alpine" style="height: 500px" :columnDefs="columnNames" :rowData="mockData"></ag-grid-vue>
    </div>
</template>


<script lang="ts">

interface fileRow {
    invoiceID: number,
    invoiceName: string,
    invoiceDate: Date,
    createDate: Date,
}


import { defineComponent, reactive, ref } from 'vue';
import { AgGridVue } from "ag-grid-vue"
import "ag-grid-community/styles/ag-grid.css";
import "ag-grid-community/styles/ag-theme-alpine.css";


export default defineComponent({
    name: 'InvoiceManagementView',
    components: {
        AgGridVue
    },

    data() {
        return {
            mockData: [
                { invoiceID: 1, invoiceName: 'H1', ivoiceDate: '2022-08-02', createDate: '2022-08.02' },
                { invoiceID: 2, invoiceName: 'H1', ivoiceDate: '2022-08-02', createDate: '2022-08.02' },
                { invoiceID: 3, invoiceName: 'H1', ivoiceDate: '2022-08-02', createDate: '2022-08.02' },
                { invoiceID: 4, invoiceName: 'H1', ivoiceDate: '2022-08-02', createDate: '2022-08.02' },
                { invoiceID: 5, invoiceName: 'H1', ivoiceDate: '2022-08-02', createDate: '2022-08.02' },
                { invoiceID: 6, invoiceName: 'H1', ivoiceDate: '2022-08-02', createDate: '2022-08.02' },
                { invoiceID: 7, invoiceName: 'H1', ivoiceDate: '2022-08-02', createDate: '2022-08.02' },
            ],
            columnNames: [
                { field: 'invoiceID' },
                { field: 'invoiceName' },
                { field: 'ivoiceDate' },
                { field: 'createDate' }

            ]

        }

    }

})



</script>