<template>
	<div class="current__track">
		<div class="song__title">El Lápiz</div>
		<div class="song__artist">Zaider</div>
	</div>
</template>
<script>
	export default{
		name: 'PlayerMusicTitle'
	}
</script>
<style lang="css" scoped>
	.current__track
	{
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		width: 100vw;
		height: 20vh;
	}
	.song__title
	{
		width: 100vw;
		text-align: center;
		font-size: 2.4rem;
	}
	.song__artist
	{
		width: 100vw;
		text-align: center;
		font-size: 1.4rem;
		padding: 5px 0;
	}
</style>