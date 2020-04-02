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
const tableColumns = ["Name", "Country", "City", "Time","Comments"];
const tableData = [
  {
    id: 1,
    name: "Bob",
    country: "Niger",
    city: "Oud-Turnhout",
    time :"5:00 am",
    comments : " good ",
  },
  {
    id: 2,
    name: "Emma",
    time: "7:89 am",
    country: "Curaçao",
    city: "Sinaai-Waas",
    comments : " good ",
  },
  {
    id: 3,
    name: "Alice",
    time: "1:42 pm",
    comments : " good ",
    country: "Netherlands",
    city: "Baileux"
  },
  {
    id: 4,
    name: "Philips ",
    time: "7:35 am",
    comments : " good ",
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
        title: "Table on Plain Background",
        columns: [...tableColumns],
        data: [...tableData]
      }
    };
  }
};
</script>
<style>
</style>
