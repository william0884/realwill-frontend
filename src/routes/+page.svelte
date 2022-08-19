<script>
    import { writable } from 'svelte/store';
    let date = new Date()


export const user = writable({
  firstname: "",
  lastname: "",
  gender: "",
  email: "",
  date: "",
  
})
</script>

<h1>Verified identity data</h1>
<form class="content">
  <label>First Name</label>
  <input type="text" bind:value={$user.firstname} />
  <label>Last Name</label>
  <input type="text" bind:value={$user.lastname} />
  <label for="gender" id="gender">Gender</label>
  <select bind:value={$user.gender} name="gender" id="gender">
    <option value="male">Male</option>
    <option value="female">Female</option>
  </select>
  <label>Date of Birth</label>
  <input type="date" bind:value={$user.date}>


</form>
<p>
	{JSON.stringify($user, 0, 2)}</p>

