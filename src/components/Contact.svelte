<script>
    import { blur, fly } from 'svelte/transition'
    export let visible = ''
</script>

{ #if visible === 'contact' }
<div class='w-80'>
<h2  in:fly='{{ delay: 1000, x: 200, duration: 2000 }}' 
    class='text-2xl font-semibold mt-2 mb-1'>Contact</h2>
<div in:blur='{{ delay: 1000, duration: 2500 }}'>w54wei@uwaterloo.ca</div>
</div>
{ /if }
