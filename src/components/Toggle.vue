<script>
    export default {
	name: 'Toggle',
	components: {
	},
	data: () => {
		return {
			isDarkTheme: localStorage.getItem('theme') === 'dark'
		}
	},
	watch: {
		isDarkTheme: {
			handler(val) {
				const theme = val ? 'dark' : 'light';
				document.documentElement.setAttribute('data-theme', theme);
				localStorage.setItem('theme', theme);
			},
			immediate: true
		}
	}
}
</script>

<template>
    <div class="toggle">
        <p>Dark Mode</p>
        <label class="switch">
            <input v-model="isDarkTheme" id="toggle_checkbox" type="checkbox" aria-label="Toggle to change theme">
            <span class="slider round"></span>
        </label>
    </div>
</template>


<style scoped>

/* The switch - the box around the slider */
.toggle {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: var(--Text);
}
.switch {
    position: relative;
    display: inline-block;
    width: 3.1rem;
    height: 1.6rem;
}

/* Hide default HTML checkbox */
.switch input {
    opacity: 0;
    width: 0;
    height: 0;
}

/* The slider */
.slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(90deg, hsl(210, 78%, 56%), hsl(146, 68%, 55%));
    -webkit-transition: .5s;
    transition: .5s;
}

.slider:before {
    position: absolute;
    content: "";
    height: 1.1rem;
    width: 1.1rem;
    right: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: .5s;
    transition: .5s;
}

input:checked + .slider {
    background: linear-gradient(90deg, hsl(210, 78%, 56%), hsl(146, 68%, 55%));
}

input:focus + .slider {
    box-shadow: 0 0 1px hsl(236, 72%, 79%);
}

input:checked + .slider:before {
    background-color: hsl(232, 19%, 15%);
    -webkit-transform: translateX(-24px);
    -ms-transform: translateX(-24px);
    transform: translateX(-24px);
}

/* Rounded sliders */
.slider.round {
    border-radius: 2rem;
}

.slider.round:before {
    border-radius: 50%;
}

@media screen and (min-width: 900px) {
    .toggle {
        column-gap: 1rem;
    }
}
</style>