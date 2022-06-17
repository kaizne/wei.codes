<script>
    import Intro from '../components/Intro.svelte'
    import Work from '../components/Work.svelte'
    import Projects from '../components/Projects.svelte'
    import Contact from '../components/Contact.svelte';
    let select = ''
</script>

<head>
    <link rel='preconnect' href='https://fonts.googleapis.com'>
    <link rel='preconnect' href='https://fonts.gstatic.com'>
    <link href='https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&display=swap' rel='stylesheet'>
    <title>wei.codes</title>
</head>

<div class='grid place-content-center w-screen h-screen font-poppins bg-gray-50'>
    <Intro bind:select='{select}' />
    <Work     visible={select} />
    <Projects visible={select} />
    <Contact  visible={select} />
</div>
