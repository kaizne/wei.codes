<script>
    import { blur, fly } from 'svelte/transition'
    export let visible = ''
</script>

{ #if visible === 'work' }
<div class='w-80'>
<h2  in:fly='{{ delay: 1000, x: 200, duration: 2000 }}' 
     class='text-2xl font-semibold mt-2 mb-1'>Work History</h2>
<div class='flex flex-col gap-y-2'>
<div in:fly='{{ delay: 1200, y: 200, duration: 2000 }}' 
     class='flex flex-row bg-white shadow p-2 rounded'>
    <img src='newton.png' alt='Newton'
         in:fly='{{ delay: 1200, y: 200, duration: 2000 }}'
         class='rounded w-20 h-20'/>
    <div class='flex flex-col justify-center ml-3'>
        <div in:blur='{{ delay: 1200, duration: 2000 }}'
             class='text-lg font-semibold'>Newton</div>
        <div in:blur='{{ delay: 1300, duration: 2000 }}' 
             class='text-md font-medium'>Software Developer Intern</div>
        <div in:blur='{{ delay: 1400, duration: 2000 }}'
             class='text-md font-normal'>May.2022 - Present</div>
    </div>
</div>
<div in:fly='{{ delay: 1600, y: 200, duration: 2000 }}' 
     class='flex flex-row bg-white shadow p-2 rounded'>
    <img src='global-reach.png' alt='Global Reach'
         in:fly='{{ delay: 1600, y: 200, duration: 2000 }}'
         class='rounded w-20 h-20'/>
    <div class='flex flex-col justify-center ml-3'>
        <div in:blur='{{ delay: 1600, duration: 2000 }}'
             class='text-lg font-semibold'>Global Reach Group</div>
        <div in:blur='{{ delay: 1700, duration: 2000 }}'
             class='text-md font-medium'>Software Developer Intern</div>
        <div in:blur='{{ delay: 1800, duration: 2000 }}'
             class='text-md font-normal'>May.2021 - Dec.2021</div>
    </div>
</div>
</div>
</div>
{ /if }
