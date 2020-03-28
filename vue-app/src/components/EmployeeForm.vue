<template>
	<!--<component @name-of-emitted-event="methodToCallOnceEmitted"></component>-->
	<div id="employee-form">
		<form @submit.prevent="handleSubmit">
			<label>Employee name</label>
			<input v-model="employee.name" type="text">
			<label>Employee email</label>
			<input v-model="employee.email" type="text">
			<button>Add Employee</button>
		</form>

		<!-- This is the same
		<form v-on:submit="handleSubmit">
		-->
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'employee-form',
		data () {
			return {
				employee: {
					name: '',
					email: ''
				},
			}
		},
		methods: {
			handleSubmit() {
				// The add:employee syntax (as opposed to add-employee or something else) is recommended in the Vue documentation
				this.$emit('add:employee', this.employee)
			}
		}
	}
</script>

<style scoped>
	form {
		margin-bottom: 2rem;
	}
</style>