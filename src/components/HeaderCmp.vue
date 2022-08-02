<template>
	<header class="header">
		<img
			src="../../public/img/Zj8_PniLP1ZNMNJYGlvtv0MjFF28VtyQ5F-1gr6Rk29GSepmOlgxbveVgmwaqIjmeM1p4ba3.jpg"
		/>
		<div>
			<h1>Идеи обретают форму</h1>
			<br />
			<h2>Мастерская по художественной ковке в городе Ломоносов.</h2>
			<h2>Делаем изделия на заказ или по вашему выбору.</h2>

			<a>Получить изделие</a>
		</div>
	</header>
</template>

<style lang="scss" scoped>
img {
	filter: brightness(50%);
	height: 100%;
	width: 100%;
}

header {
	div {
		margin: 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		position: absolute;
		border-radius: 5%;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		background-color: #00000077;
		padding: 2rem;
		h1,
		h2 {
			text-align: center;
			color: #fff;
			padding: 0;
			margin: 0;
		}

		a{
			color:#fff;
			margin: 1.5rem;
			border: 1px solid #fff;
			padding: 1rem;
		}
	}
}

@media screen and (max-width: 799px) {
	img {
		height: 100%;
		width: 200%;
		transform: translate(-35%, 0%);
		filter: brightness(30%);
	}

	header div {
		font-size: 0.55rem;
		top: 40%;
		left: 50%;
		transform: translate(-50%, -50%);

		
	}
}
</style>
