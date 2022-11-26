<script>
  export let color;
	import { createEventDispatcher } from 'svelte';
	
	let dispatch = createEventDispatcher();
</script>

<svg
  on:click={() => dispatch("click")}
  style="color:{color};" 
  width="95%"
  height="95%"
  aria-hidden="true"
  focusable="false"
  data-prefix="fas"
  data-icon="record-vinyl"
  class="svg-inline--fa fa-record-vinyl fa-w-16"
  role="img"
  xmlns="http://www.w3.org/2000/svg"
  viewBox="0 0 512 512"
>
  <path
    class="vinylBtn"
    fill="currentColor"
    d="M256 152a104 104 0 1 0 104 104 104 104 0 0 0-104-104zm0 128a24
      24 0 1 1 24-24 24 24 0 0 1-24 24zm0-272C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm0 376a128 128 0 1 1 128-128 128 128 0 0 1-128 128z"
  />
</svg>

<style>
  .vinylBtn:hover {
    animation: shake 0.5s;

    /* When the animation is finished, start again */
    animation-iteration-count: infinite;
  }

  @keyframes shake {
    0% {
      transform: translate(1px, 1px) rotate(0deg);
    }
    10% {
      transform: translate(-1px, -2px) rotate(-1deg);
    }
    20% {
      transform: translate(-3px, 0px) rotate(1deg);
    }
    30% {
      transform: translate(3px, 2px) rotate(0deg);
    }
    40% {
      transform: translate(1px, -1px) rotate(1deg);
    }
    50% {
      transform: translate(-1px, 2px) rotate(-1deg);
    }
    60% {
      transform: translate(-3px, 1px) rotate(0deg);
    }
    70% {
      transform: translate(3px, 1px) rotate(-1deg);
    }
    80% {
      transform: translate(-1px, -1px) rotate(1deg);
    }
    90% {
      transform: translate(1px, 2px) rotate(0deg);
    }
    100% {
      transform: translate(1px, -2px) rotate(-1deg);
    }
  }
</style>
