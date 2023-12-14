<template>

<div v-for="(dt, index) in data" :key="index">
    <div class="">
        <VTable
            :is-loading="false"
            :items="dt.body"
            :with-pagination="false"
            :has-error="false">
            <template #row="{item, columns}">
                <tr>
                    <component
                        :is="column"
                        v-for="(column, index) of columns"
                        :key="index"
                    />
                </tr>
            </template>

            <VColumn field="column1">
                <template #header>
                         <span class="fs-2 fw-medium text-mute">
                             {{ $t('column1') }}
                         </span>
                </template>
                <template #body="{item}">
                    {{ item.column1 }}
                </template>
            </VColumn>

            <VColumn field="column2">
                <template #header>
                         <span class="fs-2 fw-medium text-mute">
                             {{ $t('column1') }}
                         </span>
                </template>
                <template #body="{item}">
                    {{ item.column2 }}
                </template>
            </VColumn>

            <VColumn field="column3">
                <template #header>
                         <span class="fs-2 fw-medium text-mute">
                             {{ $t('column3') }}
                         </span>
                </template>
                <template #body="{item}">
                    {{ item.column3 }}
                </template>
            </VColumn>

            <VColumn field="column4">
                <template #header>
                         <span class="fs-2 fw-medium text-mute">
                             {{ $t('column4') }}
                         </span>
                </template>
                <template #body="{item}">
                    {{ item.column4 }}
                </template>
            </VColumn>

            <VColumn field="column5">
                <template #header>
                         <span class="fs-2 fw-medium text-mute">
                             {{ $t('column5') }}
                         </span>
                </template>
                <template #body="{item}">
                    {{ item.column5 }}
                </template>
            </VColumn>

        </VTable>
    </div>
</div>
</template>

<script>
import {ref} from "vue";
import VTable from "@/components/data-table/VTable.vue";
import VColumn from "@/components/data-table/VColumn.vue";

export default {

    name: "ListView",
    components: {VColumn, VTable},


    setup() {
        const data = ref([
            {
                header: {
                    header1: 'header1',
                    header2: 'header2',
                    header3: 'header3',
                    header4: 'header4',
                    header5: 'header5',
                },
                body: [
                    {
                        column1: 'column1',
                        column2: 'column2',
                        column3: 'column3',
                        column4: 'column4',
                        column5: 'column5',
                    },
                    {
                        column1: 'column11',
                        column2: 'column22',
                        column3: 'column33',
                        column4: 'column44',
                        column5: 'column55',
                    }
                ]
            }
        ]);


        return {
            data
        };
    }


}


</script>
