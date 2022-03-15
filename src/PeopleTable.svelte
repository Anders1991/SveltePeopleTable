<script>
import faker from "@faker-js/faker";
import TableHead from "./TableHead.svelte";
import TableRow from "./TableRow.svelte";

			let fakeData = [];
			let finalArray = [];
			let id = -1;

			for (let i = 0; i <= 5; i++ ) {
         		let first_name = faker.name.firstName();
         		let last_name = faker.name.lastName();
		 		let avatar = faker.image.avatar();
				id++;
				let fakeData = [{id, first_name, last_name, avatar}];
				finalArray.push(...fakeData);
			};
			
</script>

	<table>
	  <thead>
		<TableHead />
		<tr>
			<TableRow data={finalArray}/>
		</tr>
	  </thead>
	</table>

<style>

	table {
		min-width: 1000px;
	}

</style>