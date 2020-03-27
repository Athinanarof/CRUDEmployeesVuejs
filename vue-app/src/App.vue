<template>
	<div id="app" class="small-container">
		<h1>Employees</h1>

		<employee-table :employees="employees"/>

		<!-- this is the same thing-->
		<!--
		<employee-table v-bind:employees="employees" />
		-->

	</div>
</template>

<script type="text/javascript">
	import EmployeeTable from '@/components/EmployeeTable.vue'

	export default 
	{
		name: 'app',
		components: {
			EmployeeTable
		},
		data() {
			return {
				employees: [
				{

					id: 1,
					name: 'Richard Hendricks',
					email: 'richard@piedpiper.com',
				},
				{
					id: 2,
					name: 'Bertram Gilfoyle',
					email: 'gilfoyle@piedpiper.com',
				},
				{
					id: 3,
					name: 'Dinesh Chugtai',
					email: 'dinesh@piedpiper.com',
				}
				]
			}
		},
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