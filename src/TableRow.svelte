<script>
export let data = [];
</script>

<ul>
    {#each data as {id,first_name, last_name, avatar}}
	<tr>
        <li>
			{id}
		</li>
        <li>
            {first_name}
        </li>
        <li>
            {last_name}
        </li>
        <li>
            <img src={avatar} alt="Not found">
        </li>
    </tr>	
	{/each}
</ul>

<style>

    ul {
        display: flex;
        justify-content:space-around;
        align-content: center;
        flex-direction: column;
        list-style: none;    
    }

    tr {
        display: flex;
        justify-content:space-around;
        align-content: center;
        flex-direction: row;
    }

    li {
        display: flex;
        align-items: center;
    }

</style>