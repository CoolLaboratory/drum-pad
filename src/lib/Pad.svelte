<style>

  div {
    display: grid;
    place-items: center;
    background: radial-gradient( #ffab91, #ff7043);
  }

  img {
    aspect-ratio: 1;
    width: 40%;
  }

</style>

<script context="module">
  import {Howl, Howler} from 'howler';

  import mp3 from '../assets/drums/drums_drums.mp3'
  import webm from '../assets/drums/drums_drums.webm'

  let sprite = new Howl({
      src: [mp3, webm],
      sprite: {
        clap: [ 0, 734.2630385487529 ],
        closedHihat: [ 2000, 445.94104308390035 ],
        crash: [ 4000, 1978.6848072562354 ],
        kick: [ 7000, 553.0839002267571 ],
        openHihat: [ 9000, 962.7664399092968 ],
        snare: [ 11000, 354.48979591836684 ]
      }
    })

</script>

<script lang="ts">
  export let icon
  export let sound
  // export let src
</script>

<div on:click={() => sprite.play(sound)}>
  <img src={icon} alt={'icon'} />
</div>