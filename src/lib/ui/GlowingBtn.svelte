<script>
	export let text = '';
	export let href = '';
	export let fontSize = '16px'; // default font size
	export let className = '';
</script>

<a {href} target="_blank" class="btn {className}" style="font-size: {fontSize};">
	{text}
</a>

<style>
	.btn {
		background: #ff8b92;
		box-shadow: 0px 0px 10px #ff2358;
		border-radius: 40px;
		border: none;
		width: 100%;
		max-width: 758px;
		padding: 10px 16px;
		text-align: center;
		color: #343045;
		font-weight: 400;
		line-height: 28px;
		position: relative;
		display: inline-block;
		cursor: pointer;
		overflow: hidden;
		transition: all 0.5s ease;
	}

	.btn:before {
		content: '';
		position: absolute;
		top: 0;
		left: -100%;
		width: 100%;
		height: 100%;
		background-color: rgba(255, 255, 255, 0.2);
		opacity: 0;
		transition: all 0.3s ease;
	}

	.btn:hover {
		background-color: #eb737b;
		box-shadow: 0px 0px 37px #ff2358;
		color: #fff;
	}

	.btn:hover:before {
		left: 100%;
		opacity: 1;
	}
</style>
