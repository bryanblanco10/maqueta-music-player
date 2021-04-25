<template>
	<div class="vinyl">
		<div class="vinyl__container">
			<div class="vinyl__record">
				<div class="vinyl__record--image">
					<div class="vinyl__record--hole"></div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default{
		name: 'PlayerAnimation'
	}
</script>
<style lang="css" scoped>
	.vinyl{
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100vw;
		height: 50vh;
	}

	.vinyl__container{
		border-radius: 50%;
		padding: 16px;
		background-color: #eee;
		box-shadow: inset 0 1px 2px rgba(0,0,0, .4),
								0 -1px 1px #fff,
								0 1px 0 #fff;
		border-bottom: 1px solid #ddd;
	}

	.vinyl__record
	{
		display: flex;
		justify-content: center;
		align-items: center;
		width: 40vh;
		height: 40vh;
		border-radius: 50%;
		background:
			linear-gradient(30deg, transparent 40%, rgba(51,51,51,0.8) 40%) no-repeat 100% 0,
			linear-gradient(60deg, rgba(51,51,51,0.8) 60%, transparent 40%) no-repeat 0 100%,
			repeating-radial-gradient(#333, #333 9px, #ccc 10px, #333 11px);
		background-size: 50% 100%, 100% 50%, 100%;
		animation: vinyl-moving 2s ease-in-out infinite;
	}

	.vinyl__record--image
	{
		display: flex;
		justify-content: center;
		align-items: center;
		border: 1px solid #000;
		border-radius: 50%;
		width: calc(40vh - 60%);
		height: calc(40vh - 60%);
		background: url('../assets/img/perfect.jpg') no-repeat center;
		background-size: cover;
		animation: image-rotate 3s linear infinite;
	}

	.vinyl__record--hole
	{
		width: 20px;
		height: 20px;
		border-radius: 50%;
		background-color: #b5d0e6;
	}

	@keyframes image-rotate
	{
		from{
			transform: rotate(0deg);
		}
		to{
			transform: rotate(360deg);
		}
	}

	@keyframes vinyl-moving{
		0%{
			transform: rotate(0deg);
		}
		50%{
			transform: rotate(5deg);
		}
		100%{
			transform: rotate(0deg);
		}
	}
</style>