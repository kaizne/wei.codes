<script>
    import { blur, fly } from 'svelte/transition'

    export let visible = ''
</script>

{ #if visible === 'projects' }
<div class='w-80 mt-1'>
<h2  in:fly='{{ delay: 1000, x: 200, duration: 2000 }}'
     class='text-2xl font-semibold mt-2 mb-1'>Projects</h2>
<div class='flex flex-col gap-y-3'>
<div in:fly='{{ delay: 1200, y: 200, duration: 2000 }}'  
     class='flex flex-row bg-white shadow p-2 rounded'>
    <img src='quizultra.png' alt='QuizUltra'
         in:fly='{{ delay: 1200, y: 200, duration: 2000 }}'
         class='rounded w-20 h-20'/>
    <div class='flex flex-col justify-center ml-3'>
        <div in:blur='{{ delay: 1200, duration: 2000 }}'
             class='text-lg font-semibold
             text-blue-400 underline hover:cursor-pointer'>
             <a href='https://www.quizultra.com/' target='_blank'>QuizUltra</a></div>
        <div in:blur='{{ delay: 1300, duration: 2000 }}'
             class='text-md font-normal'>React Web App</div>
    </div>
</div>
<div in:fly='{{ delay: 1500, y: 200, duration: 2000 }}'  
     class='flex flex-row bg-white shadow p-2 rounded'>
    <img src='roll-3d.png' alt='Roll 3D'
         in:fly='{{ delay: 1500, y: 200, duration: 2000 }}'
         class='rounded w-20 h-20'/>
    <div class='flex flex-col justify-center ml-3'>
        <div in:blur='{{ delay: 1500, duration: 2000 }}'
             class='text-lg font-semibold
             text-blue-400 underline hover:cursor-pointer'>
             <a href='https://apps.apple.com/dk/app/roll-3d/id1579417286' target='_blank'>Roll 3D</a></div>
        <div in:blur='{{ delay: 1600, duration: 2000 }}'
             class='text-md font-normal'>IOS Mobile Game</div>
    </div>
</div>
<div in:fly='{{ delay: 1800, y: 200, duration: 2000 }}' 
     class='flex flex-row bg-white shadow p-2 rounded'>
    <img src='block-url.png' alt='Block URL'
         in:fly='{{ delay: 1800, y: 200, duration: 2000 }}'
         class='rounded w-20 h-20 border-2'/>
    <div class='flex flex-col justify-center ml-3'>
        <div in:blur='{{ delay: 1900, duration: 2000 }}'
             class='text-lg font-semibold
             text-blue-400 underline hover:cursor-pointer'>
             <a href='https://chrome.google.com/webstore/detail/block-url-website-blocker/hciflkkadhmficnfopeojmdfjfcaoejf?hl=en' target='_blank'>
               Block URL</a>
          </div>
        <div in:blur='{{ delay: 2000, duration: 2000 }}' 
             class='text-md font-normal'>Chrome Extension</div>
    </div>
</div>
</div>
</div>
{ /if }
