<script>
  import HowTo from 'components/HowTo.svelte'
  import Timer from 'components/Timer.svelte'

  let audio

</script>

<style>
  h1 {
    text-align: center;
  }
</style>

<h1>Handwashing app</h1>

<Timer on:done={ () => audio.play() }/>

<HowTo />

<audio bind:this={audio}>
  <source src="sounds/oh-yeah.wav" />
</audio>