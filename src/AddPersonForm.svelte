<script>
    let name; 
    let beltColor;
    let age;

    // let fighting, sneaking, running = false;
    let Skills = [];


const handleSubmit = () => {
    console.log(name, beltColor, age, Skills);
};

</script>

<form on:submit|preventDefault={handleSubmit}>
    <input type="text" placeholder="name" bind:value={name}>
    <input type="number" placeholder="age" bind:value={age}>
    <label>Skills:</label>
    <input type="checkbox" bind:group={Skills} value="fighting">fighting<br>
    <input type="checkbox" bind:group={Skills} value="sneaking">sneaking<br>
    <input type="checkbox" bind:group={Skills} value="running">running<br>
    <label>Belt color:</label>
    <select bind:value={beltColor}>
        <option value="black">black</option>
        <option value="orange">orange</option>
        <option value="brown">brown</option>
        <option value="white">white</option>
    </select>
    <button>Add Person</button>
</form>

<style>

</style>