<script></script>
<template>
	<div class="priorGuess" v-for="guess in priorGuesses">
		<div v-for="item in guess.result" class="letter" :class="item.score">
			{{ item.guess }}
		</div>
	</div>
</template>
<style>
.priorGuess > * {
	font-size: 40px;
	text-align: center;
	font-weight: 700;
	color: #ffffff;
	text-transform: uppercase;

	width: 2ch;
	padding: 10px;
	background-color: #3a3a3c;
	border: 2px solid #3a3a3c;
	border-radius: 5px;

	&:focus {
		outline: 2px solid #7575d3;
	}
}

.priorGuess {
	display: flex;
	gap: 10px;

	& .letter {
		/*	use this to animate the reveals: https://codepen.io/kanishkkunal/pen/wgEBgX?editors=0110*/
		&.correct {
			background-color: #538d4e;
			border: 2px solid #538d4e;
		}

		&.partial {
			background-color: #b59f3b;
			border: 2px solid #b59f3b;
		}
	}
}
</style>
