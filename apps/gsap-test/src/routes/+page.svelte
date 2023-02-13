<script lang="ts">
	import gsap from 'gsap';
	import { onMount } from 'svelte';
	onMount(() => {
		const tl = gsap.timeline();
		const duration = 2;

		tl.to('#test', {
			duration
		}).from(
			'#test',
			{
				duration,
				yPercent: 50,
				ease: 'bounce.out',
			},
			`-=${duration * 0.75}`
		);

		// gsap.timeline({
		// 		// paused: true,
		// 		defaults: { duration: 3 }
		// 	})
		// 	.to('#divtest', { opacity: 0 })
		// 	.set('#divtest', { backgroundColor: 'red', innerText: 'End the test.' })
		// 	.to('#divtest', { opacity: 1 }, '+=1');
	});
</script>

<div id="test" class="flex flex-col items-center gap-5 mx-60 my-10">
	<h1 class="text-slate-300">Bös</h1>
	<p>
		Löksås ipsum annat om kan hans i enligt annan, i och som att kom från upprätthållande tidigare,
		åker hwila från dimma tidigare hav redan. Händer dunge helt vi tre det varit dock så blev mjuka,
		räv upprätthållande plats brunsås och smultron jäst äng. Jäst stora blev vidsträckt sjö precis
		händer sjö dunge som upprätthållande och sig vad tidigare fram dunge, tre år det helt smultron
		ta stora annat rännil trevnadens hela stora göras att. Hav av blev där björnbär bäckasiner rot
		från enligt, smultron dimma nya sin när där har flera gör, jäst år trevnadens kan björnbär
		dimmhöljd verkligen. Enligt gamla brunsås därmed händer samma ska dimmhöljd, söka regn strand
		ordningens ser faktor se, jäst träutensilierna brunsås ingalunda sax som. Ingalunda både år
		händer samma göras strand söka det som, i erfarenheter dock strand från enligt händer smultron.
		År åker brunsås bra vid genom lax att tre flera söka mot så, redan jäst händer räv omfångsrik
		ser och mjuka bra ser upprätthållande, när flera regn mot stig kanske äng bäckasiner miljoner på
		därmed. Hwila se sax strand räv händer sällan björnbär tiden när, icke därmed upprätthållande
		miljoner groda är på del både, bäckasiner och år dimmhöljd ännu äng bland rot. Stora blivit och
		tre annat är se lax, denna hav söka ännu precis sista, tid genom sällan göras mot miljoner.
		Olika varit händer mot häst ännu där det tid, jäst räv från på det precis från ser annat, helt
		av blivit därmed jäst lax äng. Av blivit räv flera, där.
	</p>
</div>

<div id="divtest">Start the test.</div>

<style>
	#divtest {
		width: 200px;
		height: 200px;
		margin-top: 10px;
		color: white;
		background-color: blue;
	}
</style>
