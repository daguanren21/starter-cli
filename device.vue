<script setup lang="ts">
// Auto-generated file
import { DataTableColumns } from 'naive-ui'
export interface Device {
  serialNumber: string
}
const columns: DataTableColumns<Device> = [
  { title: 'serialNumber', key: 'serialNumber', align: 'center' },
]
let {
  loading,
  loadData,
  renderCell,
  handleResetSearch,
  searchParams,
  tableRef,
  handleChangePage,
  handleUpdateFilter,
  handleChangePageSize,
  handleUpdateSorter,
  pagination,
  tableData,
} = useTable({ fetch: fetchDevices, params: initParams })
</script>
<template>
  <n-data-table
    :row-key="(item) => item.id"
    ref="tableRef"
    @update:filters="handleUpdateFilter"
    :renderCell="renderCell"
    :loading="loading"
    @update:page="handleChangePage"
    @update:page-size="handleChangePageSize"
    remote
    :pagination="pagination"
    @update:sorter="handleUpdateSorter"
    :data="tableData"
    class="w-full flex-1"
    :columns="columns"
  ></n-data-table>
</template>
