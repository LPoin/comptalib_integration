<template>
	<div>
		<h1>{{ title }}</h1>
		<p>{{ description }}</p>
		<button @click="onClick">{{ buttonTitle }}</button>
		<hr />
		<hr />
		<div>
			<input type="radio" id="left" name="drone" value="left" v-model="picked" checked />
			<label for="left">Left</label>
		</div>
		<div>
			<input type="radio" id="right" name="drone" value="right" v-model="picked" />
			<label for="right">Right</label>
		</div>
		<div v-bind:style="{ textAlign: picked }">
			<img
				src="https://image.shutterstock.com/image-photo/medieval-knight-sword-shield-against-600w-123745765.jpg"
				alt="Knight photography"
			/>
		</div>
	</div>
</template>

<script>
export default {
	name: "CompoTest",
	data() {
		return {
			picked: "left",
			translate: false,
			title: "This is a component",
			description: "This component is called in the Image.vue page",
			buttonTitle: "Switch to french",
		};
	},
	methods: {
		onClick() {
			if (this.translate) {
				this.title = "This is a component";
				this.description = "This component is called in the Image.vue page";
				this.buttonTitle = "Switch to french";
				this.translate = !this.translate;
			} else {
				this.title = "Ceci est un composant";
				this.description = "Ce composant est appelé dans la page Image.vue";
				this.buttonTitle = "Traduire en anglais";
				this.translate = !this.translate;
			}
		},
	},
};
</script>

<style scoped>
.img {
	text-align: right;
}
</style>
