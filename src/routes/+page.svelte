<script>
	import { onMount } from 'svelte';
	import FaqElement from '../components/FaqElement.svelte';
	import MapPane from '../components/MapPane.svelte';
	import OrganizerProfile from '../components/OrganizerProfile.svelte';
	import Section from '../components/Section.svelte';

	let scrolled = false;
	onMount(() => {
		window.onscroll = (_) => {
			scrolled = window.scrollY > 40;
		};
		scrolled = window.scrollY > 40;
	});
</script>

<svelte:head>
	<title>RidgeHacks 2023</title>
	<meta
		name="description"
		content="Ridgehacks 2023 is Ridge High School's premier annual Hackathon led by the Ridge Computer Science Club."
	/>
	<meta property="og:title" content="RidgeHacks 2023" />
	<meta
		property="og:description"
		content="Ridgehacks 2023 is Ridge High School's premier annual Hackathon led by the Ridge Computer Science Club."
	/>
	<meta
		property="og:image"
		content="https://ridgecompsci.club/images/ridgehacks_background_graphic.svg"
	/>
</svelte:head>

<main class="container" class:scrolled>
	<a
		class="logo"
		tabIndex={0}
		on:click={(_) => {
			setTimeout(() => {
				window.scrollTo({
					top: 0,
					behavior: 'smooth'
				});
			}, 40);
		}}
		href="#"
	>
		<svg viewBox="0 0 113 48" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path
				d="M4.36364 43.3636V4.09091H13.0909V8.45455H8.72727V39H13.0909V43.3636H4.36364ZM69.7543 43.3636V39H74.1179V8.45455H69.7543V4.09091H78.4815V43.3636H69.7543ZM87.1875 34.6364V30.2727H91.5511V25.9091H87.1875V21.5455H91.5511V17.1818H95.9148V21.5455H100.278V17.1818H104.642V21.5455H109.006V25.9091H104.642V30.2727H109.006V34.6364H104.642V39H100.278V34.6364H95.9148V39H91.5511V34.6364H87.1875ZM95.9148 30.2727H100.278V25.9091H95.9148V30.2727Z"
			/>
			<path
				fill-rule="evenodd"
				clip-rule="evenodd"
				d="M25 11.9208H27.4V35.6832H25V44H40.2V35.6832H37.8V27.3663H44.2L45.8 28.9505V44H59V35.6832H56.2V25.7822L53.4 23.0099L56.2 20.2376V9.94059L50.2 4H25V11.9208ZM37.8 11.9208V19.0495H44.2L45.8 17.5V13.6374L44.2 11.9208H37.8Z"
			/>
		</svg>

		<span class="material-icons">expand_less</span>
	</a>
	<div class="links">
		<a href="#schedule">Schedule</a>
		<a href="#event-details">Event Details</a>
		<a href="#what-is-a-hackathon">What is a Hackathon?</a>
		<a href="#faq">FAQ</a>
		<a href="#map">Map</a>
		<a href="#speakers">Speakers</a>
		<a href="#sponsors">Sponsors</a>
		<a href="#organizers">Organizers</a>

		<a
			style="color:var(--text-accent);"
			href="https://organize.mlh.io/participants/events/9287-ridgehacks2023"
			>Register
		</a>
	</div>
	<div class="sections">
		<Section>
			<h1>Welcome to RidgeHacks!</h1>
			<p>
				Please make sure you have filled out the <a
					href="https://organize.mlh.io/participants/events/9287-ridgehacks2023"
					target="_blank">MLH Form</a
				>
				and our <a href="https://tally.so/r/3Eqe02" target="_blank">Tally Form</a> in order to participate.
			</p>
			<p>
				Have a song request for the cafeteria playlist? Submit them <a
					href="https://forms.gle/St5Pi9tH2sMmTjhF8"
					target="_blank">here</a
				>!
			</p>
			<p>
				Make sure you all have your team cards (the one with the numbers)! They are used for judging
				and are really important. If you need a card see Rachel in the Cafe.
			</p>
			<p>
				<a
					href="https://docs.google.com/presentation/d/1TeJ7UoQT1B_7H1wG8oYHfigU8R6-nhqcVEvJ4UdKAHE/edit?usp=sharing"
					>Find the opening ceremony slides here.</a
				>
			</p>
		</Section>
		<Section id="home">
			<h1>
				<span style="color:var(--text-accent);"> RidgeHacks 2023</span> -
				<span style="font-weight:400;">April 1st, 2023</span>
			</h1>
			<p>
				Ridgehacks 2023 is Ridge High School's premier annual hackathon led by the Ridge Computer
				Science Club. Following a single day, <b> 12-hour hacking schedule </b>, Ridgehacks offers a
				free hackathon for Middle and High School Students from <b>8:00 AM until 10:00 PM</b>.

				<br />
				<br />
				From all of us at RCSC, happy hacking and we hope to see you there!
			</p>

			<p>
				<b>
					Make sure to sign-up
					<span style="color:var(--text-accent);">
						<a href="https://organize.mlh.io/participants/events/9287-ridgehacks2023">here</a>!
					</span>
				</b>
			</p>

			<p>
				<b>
					Join our Discord server for announcements
					<span style="color:var(--text-accent);">
						<a href="https://discord.gg/NDpKwGG5Np">here</a>!
					</span>
				</b>
			</p>
		</Section>
		<Section id="schedule">
			<h1><span style="color:var(--text-accent);">Schedule </span></h1>

			<table class="scheduleTable">
				<thead>
					<th>Time</th>
					<th>Hacking/Main Areas</th>
					<th>Lecture Hall A</th>
					<th>Room 701</th>
					<th>PAC</th>
				</thead>
				<tr>
					<td>8:00 AM</td>
					<td>Doors Open For Participants</td>
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>8:15 AM</td>
					<td />
					<td />
					<td />
					<td style="color:var(--text-accent);">Opening Ceremony</td>
				</tr>
				<tr>
					<td>9:00 AM</td>
					<td style="color:var(--text-accent);">Hacking begins</td>
					<td />
					<td />
					<td style="color:var(--text-accent);"><a href="/speaker-bios#rich">EEC Speaker</a></td><td
					/>
				</tr>
				<tr>
					<td>10:00 AM</td>
					<td style="color:var(--text-accent);">Breakfast</td>
					<td />
					<td>Consumer Repair Workshop sponsored by Tulls Automotive</td>
					<td />
					<td />
				</tr>
				<tr>
					<td>11:00 AM</td>
					<td />
					<td />
					<td>Open CV Workshop sponsored by Ridge Marketing</td>
					<td />
					<td />
				</tr>
				<tr>
					<td>12:00 PM</td>
					<td />
					<td
						><a href="/speaker-bios#phil"
							><span style="color:var(--text-accent);">Cyber-Case Study </span> presented by Detective
							Phil Jasina
						</a></td
					>
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>1:00 PM</td>
					<td
						><span style="color:var(--text-accent);">Lunch</span> (and Super Smash Bros Tournament)</td
					>
					<td />
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>2:00 PM</td>
					<td />
					<td
						><span style="color:var(--text-accent);">Android App Development</span> presented by Professor
						Sheusi</td
					>
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>3:00 PM</td>
					<td />
					<td>
						<a href="/speaker-bios#verizon"
							><span style="color:var(--text-accent);">Green Tech in Industry</span> - a Verizon overview
						</a>
					</td>
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>4:00 PM</td>
					<td />
					<td>Web Development with Svelte</td>
					<td>Cybersecurity Workshop sponsored by the Bernards PBA</td>
					<td />
					<td />
				</tr>
				<tr>
					<td>5:00 PM</td>
					<td />
					<td>
						<span style="color:var(--text-accent);">The Future of Programming </span>by Professor
						Thomas Calabrese</td
					>
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>6:00 PM</td>
					<td><span style="color:var(--text-accent);">Dinner</span> (and chess tournament)</td>
					<td />
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>6:30 PM</td>
					<td />
					<td />
					<td style="color:var(--text-accent);">Judges Meeting</td>
					<td />
					<td />
				</tr>
				<tr>
					<td>7:00 PM</td>
					<td />
					<td />
					<td>
						<a href="/speaker-bios#chad">
							<span style="color:var(--text-accent);"> CS as Job? </span> Experiences from Industry by
							Chad Wiedemann
						</a>
					</td>
					<td />
					<td />
				</tr>
				<tr>
					<td>8:00 PM</td>
					<td style="color:var(--text-accent);">Hardstop Hacking</td>
					<td />
					<td />
					<td />
					<td />
				</tr>
				<tr>
					<td>8:45 PM</td>
					<td />
					<td />
					<td />
					<td>Finalist Presentations</td>
					<td />
				</tr>
				<tr>
					<td>9:45 PM</td>
					<td />
					<td />
					<td />
					<td>Closing Ceremony </td>
					<td />
				</tr>
				<tr>
					<td>10:00 PM</td>
					<td style="color:var(--text-accent);">Event Ends</td>
					<td />
					<td />
					<td />
					<td />
				</tr>
			</table>
			<center
				><h3>
					<span style="color:var(--text-accent);"
						>Media Center Open for quiet hacking at all times
					</span>
				</h3></center
			>
		</Section>
		<Section id="speakers">
			<h1>Speakers</h1>
			<a href="/speaker-bios">See Speaker Bios &rarr;</a>
			<div class="bronzeSponsorLogoList">
				<a href="https://www.somersetcountyparks.org/" target="_">
					<img src={`speakers/scpc.png`} />
				</a>
				<a href="https://verizon.com" target="_">
					<img src={`speakers/verizon.svg`} />
				</a>
				<a href="https://www.bernards.org/departments/police" target="_">
					<img src={`speakers/btpd.jpg`} />
				</a>
				<a href="https://usj.edu" target="_">
					<img src={`speakers/usj.webp`} />
				</a>
			</div>
		</Section>
		<Section id="event-details">
			<h1><span style="color:var(--text-accent);">Details</span></h1>
			<div>
				<p>
					<span style="color:var(--text-accent);"><strong>Date:</strong> </span> April 1st, 2023
				</p>
				<p>
					<span style="color:var(--text-accent);"><strong>Who can attend:</strong></span> Any middle
					school or high school student (grades 6-12) who's down to make something awesome. Or anything
					tech, or programming related really (please reach out if you are an elementary student interested
					in attending).
				</p>
				<p>
					<span style="color:var(--text-accent);"><strong>Cost to attend:</strong> </span>Free!
				</p>
				<p>
					<span style="color:var(--text-accent);"><strong>Location:</strong></span> Ridge High School
					(268 South Finley Avenue, Basking Ridge, NJ).
				</p>
				<p>
					<span style="color:var(--text-accent);" /><strong>
						See the FAQ for details on where to enter (and park if you plan on driving yourself).
					</strong>
				</p>
			</div>
		</Section>
		<Section id="what-is-a-hackathon">
			<h1><span style="color:var(--text-accent);">What is a Hackathon?</span></h1>
			<p>
				A hackathon is an event where students individually or collaboratively create innovative
				solutions with technology, often using hardware, software, or both! Students present and
				share their ideas with other participants and can be awarded with prizes for their work. In
				addition, due to many workshops and experienced mentors, a hackathon is a great learning
				opportunity and experience. Overall, hackathons are an excellent event for any student with
				an interest in computer science and programming to attend, no matter the skill level.
			</p>
		</Section>
		<Section id="faq">
			<h1><span style="color:var(--text-accent);">FAQ</span></h1>

			<FaqElement summary={'Where can I park/where do I enter the building?'}>
				<p>
					Please consult the map below. Make sure to enter the building through the Performing Arts
					Center (PAC).
				</p>
			</FaqElement>

			<FaqElement summary={"Where do we get updates/communicate with y'all?"}>
				<p>
					Discord! Make sure to join our server
					<a href="https://discord.gg/NDpKwGG5Np">here</a>.
				</p>
			</FaqElement>

			<FaqElement summary={'How will teams work?'}>
				<p>
					You can work in teams of 2 to 4. If you don't have a team, don't worry! You'll be able to
					form a team at RidgeHacks with other people looking for teams or teams that want more
					members before hacking begins.
				</p>
			</FaqElement>

			<FaqElement summary={'How long is the event? When is it? Where is it?'}>
				<p>
					It's on April 1st, 2023 from 8:00AM-10:00PM. It's at Ridge High School. You can find the
					address for our hackathon
					<a href="#event-details">here</a>.
				</p>
			</FaqElement>

			<FaqElement summary={'What can I make?'}>
				<p>
					Anything. Software, hardware, middleware, malware, anything that ends with “ware” and
					starts with you typing lines of code. And even more than that!
				</p>
			</FaqElement>

			<FaqElement summary={"What's in it for me?"}>
				<p>
					Well, the clout and prestige of winning Ridgehacks(college). And of course, we do have
					prizes. You'll have to show up to find out what they are though.
				</p>
			</FaqElement>

			<FaqElement summary={'Anything else?'}>
				<p>
					Send us a message on Discord in the #FAQ channel. You can also send us an email at
					<a href="mailto:team@ridgehacks.us">team@ridgehacks.us</a>.
				</p>
			</FaqElement>
		</Section>
		<MapPane />
		<Section id={'sponsors'}>
			<h1>Sponsors</h1>
			<p>Looking to sponsor? Contact us at team@ridgehacks.us.</p>

			<h2>Emerald Sponsors</h2>
			<div id={'emerald-sponsors'} class="sponsorLogoList">
				<a href="https://mlh.io/" target="_">
					<img src={`sponsors/mlh.png`} />
				</a>
			</div>

			<h2>Gold Sponsors</h2>
			<div id={'gold-sponsors'} class="goldSponsorLogoList">
				<a href="https://www.njspba.com/" target="_">
					<img src={`sponsors/PBA.png`} />
				</a>
				<a href="https://www.perrottis.com" target="_">
					<img src={`sponsors/perrottis.png`} />
				</a>
				<a href="https://www.bernardscafe.com/" target="_">
					<img src={`sponsors/bercafe.png`} />
				</a>
				<a href="https://automationroboticsarduino.com/" target="_">
					<img src={`sponsors/gar.png`} />
				</a>
				<a href="https://buonapizzabernardsville.com/" target="_">
					<img src={`sponsors/bouna.svg`} />
				</a>
			</div>

			<h2>Silver Sponsors</h2>
			<div id={'silver-sponsors'} class="silverSponsorLogoList">
				<a href="https://www.ridgemarketing.com/" target="_">
					<img src={`sponsors/ridge_marketing.png`} />
				</a>
				<img src={`sponsors/tulls.png`} style="filter: invert(0.9);" />
				<a href="https://www.leangap.org/" target="_">
					<img src={`sponsors/leangap.svg`} />
				</a>
				<a href="https://stopandshop.com/" target="_">
					<img src={`sponsors/stopshop.svg`} />
				</a>
			</div>

			<h2>Bronze Sponsors</h2>
			<center>
				<div id={'bronze-sponsors'} class="bronzeSponsorLogoList">
					<a href="https://www.artofproblemsolving.com/" target="_">
						<img src={`sponsors/aops.png`} />
					</a>
					<a href="https://www.wegmans.com/" target="_">
						<img src={`sponsors/WegmansLogo.min.svg`} />
					</a>
					<a href="https://www.jerseymikes.com/" target="_">
						<img src={`sponsors/jmikes.png`} />
					</a>
					<a href="https://www.echo3d.co/" target="_">
						<img src={`sponsors/echo3D.png`} />
					</a>
					<img src={`/sponsors/balsamiq.png`} />
				</div>
			</center>
			<h2>Past Sponsors</h2>
			<p>RidgeHacks 2019 and 2022 would not have been possible without these sponsors.</p>
			<div class="pastSponsorLogoList">
				<a href="https://www.digitalocean.com/" target="_">
					<img src={`sponsors/digitalocean_2022.svg`} />
				</a>
				<a href="https://www.hokecapital.com/" target="_">
					<img src={`sponsors/hcmlogo-bg.png`} />
				</a>
				<a href="https://www.njspba.com/" target="_">
					<img src={`sponsors/PBA.png`} />
				</a>
				<a href="https://www.perrottis.com" target="_">
					<img src={`sponsors/perrottis.png`} />
				</a>
				<a href="https://www.ridgemarketing.com/" target="_">
					<img src={`sponsors/ridge_marketing.png`} />
				</a>
				<a href="https://www.leading-learners.com/" target="_">
					<img src={`sponsors/leading-learners.png`} />
				</a>
				<a href="https://www.echo3d.co/" target="_">
					<img src={`sponsors/echo3D.png`} />
				</a>
				<a href="https://www.wegmans.com/" target="_">
					<img src={`sponsors/WegmansLogo.min.svg`} />
				</a>
				<a href="https://www.artofproblemsolving.com/" target="_">
					<img src={`sponsors/aops.png`} />
				</a>
				<img src={`/sponsors/brba.png`} />
				<img src={`/sponsors/computersharp.png`} />
				<img src={`/sponsors/LGS.gif`} />
				<img src={`/sponsors/linode.svg`} />
				<img src={`/sponsors/intellect.png`} />
				<img src={`/sponsors/balsamiq.png`} />
				<img src={`/sponsors/aops.png`} />
				<img src={`/sponsors/gitkraken.png`} />
				<img src={`/sponsors/wolfram.png`} />
				<img src={`/sponsors/starbucks.png`} />
				<img src={`/sponsors/temboo.png`} />
				<img src={`/sponsors/bernardsvilleprint.png`} />
				<img src={`/sponsors/sketch.png`} />
			</div>
		</Section>
		<Section id={'organizers'}>
			<h1>The Organizers</h1>
			<div class="organizersList">
				<OrganizerProfile
					fullName="Michael Moschello"
					role="President of Ridgehacks"
					image="michael.jpg"
				/>
				<OrganizerProfile
					fullName="Benjamin Chee"
					role="Director of Ridgehacks"
					image="Benjamin Chee.png"
				/>
				<OrganizerProfile
					fullName="Akhil Vanka"
					role="Ridgehacks Club Director"
					image="akhil.jpg"
				/>
				<OrganizerProfile fullName="Kevin Li" role="Director of Education" image="kevin.png" />
				<OrganizerProfile fullName="Cy Westbrook" role="Technical Director" image="cy.jpg" />
				<OrganizerProfile fullName="Rachel Li" role="Lead Graphic Designer" image="rachel.jpg" />
				<OrganizerProfile fullName="Duc Nguyen" role="Lead Coordinator" image="duc.png" />
				<OrganizerProfile fullName="Brandon Li" role="Volunteer Coordinator" image="brandon.jpg" />
			</div>
		</Section>
	</div>
	<div class="logoBottom">
		<div class="bottomLogoContainer">
			<svg width="436" height="51" viewBox="0 0 436 51" xmlns="http://www.w3.org/2000/svg">
				<path
					d="M4.36364 43.3636V4.09091H13.0909V8.45455H8.72727V39H13.0909V43.3636H4.36364ZM69.7543 43.3636V39H74.1179V8.45455H69.7543V4.09091H78.4815V43.3636H69.7543ZM87.1875 34.6364V30.2727H91.5511V25.9091H87.1875V21.5455H91.5511V17.1818H95.9148V21.5455H100.278V17.1818H104.642V21.5455H109.006V25.9091H104.642V30.2727H109.006V34.6364H104.642V39H100.278V34.6364H95.9148V39H91.5511V34.6364H87.1875ZM95.9148 30.2727H100.278V25.9091H95.9148V30.2727ZM130.781 39V17.1818H148.236V25.9091H143.872V21.5455H135.145V39H130.781ZM152.578 39V34.6364H156.942V21.5455H152.578V17.1818H161.305V34.6364H165.669V39H152.578ZM156.942 12.8182V8.45455H161.305V12.8182H156.942ZM174.375 39V17.1818H187.466V8.45455H191.83V39H174.375ZM178.739 34.6364H187.466V21.5455H178.739V34.6364ZM196.172 47.7273V43.3636H209.263V39H196.172V17.1818H213.626V47.7273H196.172ZM200.536 34.6364H209.263V21.5455H200.536V34.6364ZM217.969 39V17.1818H235.423V30.2727H222.332V34.6364H235.423V39H217.969ZM222.332 21.5455V25.9091H231.06V21.5455H222.332ZM239.766 39V8.45455H244.129V17.1818H257.22V39H252.857V21.5455H244.129V39H239.766ZM261.562 39V25.9091H274.653V21.5455H261.562V17.1818H279.017V34.6364H283.381V39H261.562ZM265.926 30.2727V34.6364H274.653V30.2727H265.926ZM283.359 39V17.1818H300.814V21.5455H287.723V34.6364H300.814V39H283.359ZM305.156 39V8.45455H309.52V25.9091H318.247V30.2727H309.52V39H305.156ZM318.247 30.2727H322.611V39H318.247V30.2727ZM318.247 17.1818H322.611V25.9091H318.247V17.1818ZM326.953 39V34.6364H340.044V30.2727H326.953V17.1818H344.408V21.5455H331.317V25.9091H344.408V39H326.953ZM348.75 39V21.5455H361.841V12.8182H348.75V8.45455H366.205V25.9091H353.114V34.6364H366.205V39H348.75ZM370.547 39V8.45455H388.001V39H370.547ZM374.911 34.6364H383.638V30.2727H379.274V25.9091H383.638V12.8182H374.911V17.1818H379.274V21.5455H374.911V34.6364ZM392.344 39V21.5455H405.435V12.8182H392.344V8.45455H409.798V25.9091H396.707V34.6364H409.798V39H392.344ZM414.141 39V34.6364H427.232V25.9091H418.504V21.5455H427.232V12.8182H414.141V8.45455H431.595V39H414.141Z"
				/>
				<path
					fill-rule="evenodd"
					clip-rule="evenodd"
					d="M25 11.9208H27.4V35.6832H25V44H40.2V35.6832H37.8V27.3663H44.2L45.8 28.9505V44H59V35.6832H56.2V25.7822L53.4 23.0099L56.2 20.2376V9.94059L50.2 4H25V11.9208ZM37.8 11.9208V19.0495H44.2L45.8 17.5V13.6374L44.2 11.9208H37.8Z"
				/>
			</svg>
		</div>

		<p>
			<small>Ridge High School Hackathon, April 1st</small> <br />
			<small>268 S Finley Ave, Basking Ridge, NJ 07920</small>
			<br />
			<small>
				<a href="mailto:team@ridgehacks.us">team@ridgehacks.us</a>
			</small>
		</p>
	</div>
</main>

<style lang="scss">
	.container {
		// padding: 8px;
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		box-sizing: border-box;
		z-index: 0;
		scroll-behavior: smooth;
	}

	.header {
		width: var(--width);
		max-width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		// height: 64px;
		position: sticky;
		top: 0;
		color: #383d36;
		z-index: 0;
		// mix-blend-mode: saturation;
		> * {
			margin: 0;
			z-index: 10;
		}
	}

	.logo {
		z-index: 30;
		position: sticky;
		top: var(--section-spacing);
		height: var(--logo-height);
		margin: var(--section-spacing);
		display: flex;
		align-items: center;
		--transition: 240ms cubic-bezier(0.37, 0, 0, 1);
		// background-color: var(--bg);
		transition: padding var(--transition), gap var(--transition), background-color 120ms;
		padding-left: calc(0.5 * var(--logo-height));
		padding-right: calc(0.5 * var(--logo-height));
		border-radius: calc(0.5 * var(--logo-height));
		gap: 0px;
		> span {
			font-size: calc(0.75 * var(--logo-height));
			width: 0;
			// opacity: 0;
			transition: var(--transition);
			overflow: hidden;
		}
		> svg {
			fill: var(--text);
			height: 100%;
		}
		cursor: pointer;
	}

	.scrolled .logo {
		gap: 8px;
		padding-top: calc(0.6 * var(--section-spacing));
		padding-bottom: calc(0.6 * var(--section-spacing));
		background-color: var(--bg);
		box-shadow: 0 2px 4px 0 #2228;
		> span {
			width: calc(0.75 * var(--logo-height));
			opacity: 1;
		}
	}

	.links {
		margin-bottom: var(--section-spacing);
		position: sticky;
		top: calc(var(--logo-height) + var(--section-spacing) * 2);
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
		column-gap: 24px;
		row-gap: 8px;
		padding-inline: var(--section-spacing);
		> * {
			text-decoration: none;
			font-size: 1.2rem;
			font-weight: 600;
		}
	}

	.sections {
		width: 100%;
		padding-left: var(--section-spacing);
		padding-right: var(--section-spacing);
		// padding-bottom: var(--section-spacing);
		gap: calc(1 * var(--section-spacing));
		display: flex;
		flex-direction: column;
		align-items: center;
		background: var(--bg);
		z-index: 20;
		position: relative;
		> :global(.section) {
			background-color: var(--fg);
		}
	}

	@mixin responsive-grid-child($max-width) {
		width: 100%;
		max-height: calc($max-width * 0.5);
		object-fit: contain;
	}

	@mixin responsive-grid($max-width) {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(min($max-width, 100%), 1fr));
		gap: 48px;
		padding: 32px;
		align-items: center;
		justify-items: center;
		align-content: center;

		> :global(*) {
			@include responsive-grid-child($max-width);
		}
	}

	.scheduleTable {
		width: 100%;
		display: block;
		overflow: auto;
		border-collapse: collapse;
		tr {
			td,
			th {
				&:nth-child(1) {
					width: 10rem;
				}
				padding: 10px;
				text-align: left;
			}
			border-bottom: 2px solid var(--text-translucent);
		}
	}

	.sponsorLogoList {
		@include responsive-grid(550px);

		a img {
			@include responsive-grid-child(500px);
		}
	}
	.goldSponsorLogoList {
		@include responsive-grid(350px);

		a img {
			@include responsive-grid-child(400px);
		}
	}
	.silverSponsorLogoList {
		@include responsive-grid(300px);

		a img {
			@include responsive-grid-child(300px);
		}
	}
	.bronzeSponsorLogoList {
		@include responsive-grid(250px);

		a img {
			@include responsive-grid-child(250px);
		}
	}

	.pastSponsorLogoList {
		@include responsive-grid(150px);

		a img {
			@include responsive-grid-child(150px);
		}
	}

	.sponsorLogoList,
	.pastSponsorLogoList {
		img {
			padding: 8px;
			border-radius: 8px;
			// background-color: #fff;
			height: 100%;
			width: 100%;
		}
		a {
			width: 100%;
			height: 100%;
		}
	}

	.organizersList {
		@include responsive-grid(250px);
	}

	.logoBottom {
		// z-index: 0;
		position: sticky;
		// top: var(--section-spacing);
		bottom: 0;
		padding: var(--section-spacing);
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 8px;
		text-align: center;
		> * {
			margin: 0;
		}
	}

	.bottomLogoContainer {
		display: flex;
		justify-content: center;
		width: 100%;
		> svg {
			fill: var(--text);
			width: 100%;
			max-height: 36px;
		}
	}

	.ridgeMap {
		box-sizing: border-box;
		width: 100%;
		margin-bottom: 1rem;
	}

	:global(#sponsors, #speakers) {
		background-color: #fffc;
		color: black;
	}
</style>
