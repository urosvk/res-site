<script>
	export let names;
    let idx = names.lastIndexOf(',');
    let parsedNames = names.substring(0,idx) + " &" + names.substring(idx+1);
</script>

{parsedNames}