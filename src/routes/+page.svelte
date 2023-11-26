<script>
	import { onMount } from "svelte";

	let wants = ["Learn and grow at my own pace", "Autonomy", "The presumption of competence", "Boundaries", "Comfort", "Valued and appreciated", "Responsibility", "Community"];
	let donts = ["Absolute compliance", "Bullying", "Trickery", "Over-sexualization", "Under-sexualization", "Pretend to be \"normal\"", "Be silenced", "Excessive sheltering"];
	
	let quotes = [
		{ text: 'I encourage the parents of autistic children to do two things: develop relationships with adult autistic people when you can and consistently affirm that there are many ways of being.', author: 'Amythest Schaber' },
		{ text: 'Just because children with autism have trouble communicating does not mean they cannot communicate.', author: 'Ondrea Marisa Robinson' },
		{ text: 'My parents have always supported me, and it makes the blow of a hurtful comment so much easier to withstand.', author: 'Haley Moss' },
		{ text: 'But while you believe your child will only be happy when these things are all worked out, the truth is she will forever be happy knowing she was loved enough that you are here fighting and advocating for her.', author: 'Jennifer St. Jude' },
		{ text: 'You do not have to understand someone to love them. You dont have to agree on what brings joy or defines success to accept them and and celebrate their happiness with them.', author: 'Amethyst Schaber' },
		{ text: 'I hope you have the type of child who will live their life fearlessly, unafraid of the world ahead, and have enough to use their words or experiences to show that autism is not something to be ashamed of, embarrassed about, or an inner demon.', author: 'Haley Moss' },
		{ text: '...even though I tell you to champion your child, to be supportive and build their confidence, know that it may be torn down at some point by the outside world. In your eyes, and in mine, your child will be perfect in an imperfect world.', author: 'Haley Moss' }
	 ];
	 
	let authors = [
		'Jess Wilson',
		'B. Martin Allen',
		'Kassiane Asasumasu',
		'Katie Levin',
		'Lei Wiley-Mydske',
		'Dusya Lyubovskaya',
		'Anonymous',
		'Heidi Wangelin',
		'Karen Lean',
		'Jennifer St. Jude',
		'Ondrea Marisa Robinson',
		'Haley Moss',
		'Victoria M. Rodríguez-Roldán',
		'Amythest Schaber',
		'Kayla Smith',
		'Amelia “Mel” Evelyn Voicy Baggs',
		'Amy Sequenzia',
		'HW',
		'Morénike Giwa Onaiwu',
		'Lynne Soraya',
		'Maxfield Sparrow',
		'Anonymous',
		'Mallory Cruz',
		'Kayla Rodriguez',
		'Jean Winegardner',
		'Alexandra Forshaw',
		'Lydia X. Z. Brown',
		'Emily Paige Ballou',
		'Beth Ryan',
		'SHARON DAVANPORT'
	];

	onMount(() => {
		document.body.classList.add("bg-gray-100");
	});
</script>

<div
	class="flex flex-col items-center justify-center min-h-screen text-center bg-gray-100"
>
	<div class="p-4">
		<h1 class="text-4xl font-bold text-blue-700">
			Welcome to the Parental Handbook
		</h1>
		<p class="mt-4 text-lg text-gray-700">
			A guide for parents, sharing heartfelt experiences and wisdom from
			autistic individuals, grounded in the insights from the book
			<em>Sincerely, Your Autistic Child</em>.
		</p>
	</div>

	<svg class="mx-auto mt-10" width="400" height="300">
		<circle cx="150" cy="150" r="100" fill="red" opacity="0.5" />
		<circle cx="250" cy="150" r="100" fill="blue" opacity="0.5" />
	</svg>
</div>

<hr class="border-t border-gray-300 mx-auto w-3/4" />

<div
	class="flex flex-col items-center justify-center min-h-screen p-4 bg-gray-100"
>
	<h2 class="mb-4 text-2xl font-bold text-blue-700">
		In the Authors' Own Words
	</h2>

	<div class="flex w-full max-w-2xl justify-between">
		<div class="w-1/2 mr-2">
			<h2 class="mb-4 text-2xl font-bold text-blue-500">Wants</h2>
			<table
				class="w-full mb-8 text-center border-collapse border border-gray-300"
			>
				<tbody>
					{#each wants as want (want)}
						<tr>
							<td class="p-4 border border-gray-300 font-light">
								{want}
							</td>
						</tr>
					{/each}
				</tbody>
			</table>
		</div>

		<div class="w-1/2 ml-2">
			<h2 class="mb-4 text-2xl font-bold text-blue-500">Don'ts</h2>
			<table
				class="w-full text-center border-collapse border border-gray-300"
			>
				<tbody>
					{#each donts as dont (dont)}
						<tr>
							<td class="p-4 border border-gray-300 font-light">
								{dont}
							</td>
						</tr>
					{/each}
				</tbody>
			</table>
		</div>
	</div>
	
	<h2 class="mb-4 text-lg text-blue-500">
		Note: This is a not an exhaustive list, and if you find yourself thinking: "But every child is different!" You are on the right track.
	</h2>
</div>

<hr class="border-t border-gray-300 mx-auto w-3/4" />

<div class="flex flex-col items-center justify-center min-h-screen p-4 bg-gray-100">
  <h2 class="mb-8 text-2xl font-bold text-blue-700">Selected Quotes</h2>

  <div class="flex w-full justify-around flex-wrap">
	{#each quotes as quote (quote.text)}
	  <div class="p-4 mb-4 bg-white shadow-lg rounded w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/4 mx-2">
		<p class="mb-2 text-lg font-semibold text-gray-700">"{quote.text}"</p>
		<p class="text-sm text-gray-500">- {quote.author}</p>
	  </div>
	{/each}
  </div>
</div>

<hr class="border-t border-gray-300 mx-auto w-3/4" />

<div class="flex flex-col items-center justify-center min-h-screen p-4 bg-gray-100">
  <h2 class="mb-4 text-2xl font-bold text-blue-700">Acknowledgements</h2>
  <p class="w-3/4 text-lg text-gray-700">
	We would like to express our deepest gratitude to the authors of <em>Sincerely, Your Autistic Child</em> for their invaluable insights and contributions to the understanding of autism and the roles of a parent. This project would not have been possible without their work.
  </p>
  <p class="w-3/4 text-lg text-gray-700 mt-4">
  Authors:
  <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4 mt-2">
	{#each authors as author (author)}
	  <span>{author}</span>
	{/each}
  </div>
</div>
