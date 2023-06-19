<script>
import { fade } from 'svelte/transition'
export let select = ''
</script>

{ #key select }
<h1 
    class='text-3xl font-bold underline'>Hi, I'm  
          <span class='text-orange-400 underline decoration-orange-400'>William</span>
</h1>
<div 
     class='text-xl'>CS @ <span class='font-bold text-orange-400'>UWaterloo</span></div>
<div class='flex flex-row gap-x-4 mt-2 mb-2'>
     <a href='https://www.linkedin.com/in/wei-william/' target='_blank'>
          <img src='linkedin.png' alt='LinkedIn' class='w-12 h-10' />
     </a>
     <a href='https://github.com/Kaizne' target='_blank'>
          <img src='github.png' alt='GitHub' class='w-10 h-10' />
     </a>
     <a href='https://www.youtube.com/@KaizneCodes' target='_blank'>
          <img src='youtube.webp' alt='YouTube' class='w-13 h-10' />
     </a>
</div>
<div 
     class='flex flex-row gap-x-4 mt-2'>
     <button on:click={() => select = 'work'}
             class={`${select === 'work' ? 'bg-emerald-400 underline' :
                                           'bg-gray-300 no-underline'}
                     w-20 h-8 rounded font-medium text-white`}>
        Work
    </button>
     <button on:click={() => select = 'projects'}
             class={`${select === 'projects' ? 'bg-emerald-400 underline' :
                                               'bg-gray-300 no-underline'}
                     w-20 h-8 rounded font-medium text-white`}>
          Projects
     </button>
     <button on:click={() => select = 'contact'}
             class={`${select === 'contact' ? 'bg-emerald-400 underline' :
                                              'bg-gray-300 no-underline'}
                     w-20 h-8 rounded font-medium text-white`}>
          Contact
     </button>
</div>
{ /key }
