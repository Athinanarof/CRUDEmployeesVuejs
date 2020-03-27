<template>
	<div id="app" class="small-container">
		<h1>Employees</h1>

		<employee-table/>
	</div>
</template>

<script type="text/javascript">
	import EmployeeTable from '@/components/EmployeeTable.vue'

	export default {
		name: 'app',
		components: {
			EmployeeTable
		}
	}
</script>

<style type="text/css">
	
	button {
		background: #009435;
		boder: 1px solid #009435;
	}

	.small-container {
		max-width: 680px
	}
</style>