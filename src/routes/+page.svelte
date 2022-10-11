<script>
	import Meeting from '$lib/meeting.svelte';
	import Lockout from '$lib/lockout.svelte';
	import Contest from '$lib/contest.svelte';
	import Calforces from '$lib/calforces.svelte';

	const team = [
		{
			name: 'Xavier',
			role: 'President',
			desc: 'Hi! I’m a second-year CS + Physics major from Upstate New York.  In my free time, I enjoy competitive programming, cycling, rock climbing, skiing, and playing the piano and saxophone.'
		},
		{
			name: 'Xavier',
			desc: 'god of programming'
		},
		{
			name: 'Xavier',
			desc: 'god of programming'
		}
	];
</script>

<div class="section is-small" style="background-color: var(--blue); color: var(--grey-light)">
	<div class="container">
		<h1 class="title">Welcome to CC@B!</h1>
		<p class="paragraph">
			We are a group of students building a community around competitive coding. We aim to improve
			as a group and have fun while doing it. If this sounds good to you, we would love to have you!
			Drop by at our <a href="#">discord channel</a> and say hello :^).
		</p>
	</div>
</div>
<div class="section is-small" style="background-color: var(--yellow)">
	<div class="container">
		<h2 class="title">Activities</h2>

		<div class="group">
			<div class="group-icon">
				<Meeting />
			</div>
			<div class="group-content">
				<h3 class="subtitle">Weekly Meetings</h3>
				<p class="paragraph">
					We have weekly meetings on Mondays from 7-9 which consist of a beginner tutorial, a
					general meeting (with announcements and ICPC strategies), and an advanced topic meeting,
					in that order.
				</p>
			</div>
		</div>

		<div class="group">
			<div class="group-icon">
				<Lockout />
			</div>
			<div class="group-content">
				<h3 class="subtitle">Monthly Lockouts</h3>
				<p class="paragraph">
					Lockouts are head-to-head programming contests where two competitors race each other to
					solve problems. Contestants can solve the problems in any order and only the first person
					to solve a problem gets the points, creating an exciting game of speed and strategy. We
					host this every month and have previously organized contests against other schools!
				</p>
			</div>
		</div>

		<div class="group">
			<div class="group-icon">
				<Contest />
			</div>
			<div class="group-content">
				<h3 class="subtitle is-flat">Bi-Weekly Contests</h3>
				<p class="paragraph">
					We hold hybrid bi-weekly mock contests similar to ICPC with problems from a variety of
					sources such as Kattis and Codeforces as well as problems submitted by club members. The
					contest is 2.5 hours long, and the last half hour of the meeting reserved for solution
					discussion.
				</p>
			</div>
		</div>

		<div class="group">
			<div class="group-icon">
				<Calforces />
			</div>
			<div class="group-content">
				<h3 class="subtitle">Calforces</h3>
				<p class="paragraph">
					On the day of every rated Codeforces contest, we organize an optional virtual contest in
					the Codeforces Gym, from 7-9pm on that day. These contests allow club members to regularly
					participate in current programming contests without having to wake up too early.
				</p>
			</div>
		</div>
	</div>
</div>

<div class="section is-small">
	<div class="container">
		<h2 class="title" id="team">Team</h2>
		{#each team as person}
			<div class="card">
				<div class="card-header">{person.name} - <span class="role">{person.role}</span></div>
				<div class="card-item">{person.desc}</div>
			</div>
		{/each}
	</div>
</div>

<style>
	.group {
		display: flex;
		margin-top: 1em;
		margin-bottom: 1em;
	}

	.group-icon {
		flex: 0.8em 0 0;
		margin-top: 0.125em;
		margin-right: 8px;
	}

	.role {
		font-weight: normal;
	}
</style>
