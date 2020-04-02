<template>
    <div class="row">
      
      <div class="col-12">
        <card class="card-plain">
          <div class="table-full-width table-responsive">
            <base-table :title="table2.title" :sub-title="table2.subTitle" :data="table2.data"
                         :columns="table2.columns">

            </base-table>
          </div>
        </card>
      </div>

    </div>
</template>

<script>
import { BaseTable } from "@/components";
const tableColumns = ["Name", "Country", "City","Time"];
const tableData = [
  {
    id: 1,
    name: "Alice",
    time: "5:00 pm",
    country: "Niger",
    city: "Oud-Turnhout",
  },
  {
    id: 2,
    name: "Bob",
    time: "5:20 pm",
    country: "Curaçao",
    city: "Sinaai-Waas"
  },
  {
    id: 3,
    name: "Kevin",
    time: "5:40 pm",
    country: "Netherlands",
    city: "Baileux"
  },
  {
    id: 4,
    name: "Lily",
    time: "5:30 pm",
    country: "Korea, South",
    city: "Overland Park"
  },
  
];

export default {
  components: {
    BaseTable
  },
  data() {
    return {
      table2: {
        title: "Acorn customers",
        columns: [...tableColumns],
        data: [...tableData]
      }
    };
  }
};
</script>
<style>
</style>
