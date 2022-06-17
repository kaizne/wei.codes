<script>
import { fade } from 'svelte/transition'
export let select = ''
</script>

{ #key select }
<h1 in:fade='{{ duration: 1000 }}'
    class='text-3xl font-bold underline'>Hi, I'm  
          <span class='text-sky-400 underline decoration-sky-400'>William</span>
</h1>
<div in:fade='{{ duration: 1500 }}'
     class='text-xl'>CS @ <span class='text-sky-400'>UWaterloo</span></div>
<div in:fade='{{ duration: 2000 }}'
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
