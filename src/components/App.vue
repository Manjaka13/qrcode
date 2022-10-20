<template>
	<div class="container">
		<h1 class="container__title">QR Code generator</h1>
		<hr />
		<input
			class="container__input"
			placeholder="Enter string"
			type="text"
			v-model="url"
		/>
		<div class="container__qr">
			<vue-qrious :value="url" mime="image/webp" :size="350" />
		</div>
		<p class="container__copyright">
			Made with <span class="red">♥</span> by
			<a class="link" href="https://github.com/Manjaka13" title="Author"
				>Hari</a
			>
		</p>
	</div>
</template>

<script>
import VueQrious from "vue-qrious";

export default {
	name: "App",
	components: {
		VueQrious,
	},
	data() {
		return {
			url: "Hari",
		};
	},
	methods: {},
};
</script>
