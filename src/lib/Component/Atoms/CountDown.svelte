<script lang="ts">
	import { onMount, onDestroy } from 'svelte';

	let days: string = '0';
	let hours: string = '0';
	let minutes: string = '0';
	let seconds: string = '0';

	// Define the types explicitly for better type safety
	let targetDate: Date;
	let countdownInterval: number;

	const twentyDaysInMilliseconds = 20 * 24 * 60 * 60 * 1000;

	function updateCountdown() {
		const currentDate = new Date();
		const timeDifference = targetDate.getTime() - currentDate.getTime();

		if (timeDifference <= 0) {
			// Countdown has reached or passed the target date
			days = '0';
			hours = '0';
			minutes = '0';
			seconds = '0';

			// Restart the countdown by setting the target date to 20 days from the current date
			targetDate = new Date(currentDate.getTime() + twentyDaysInMilliseconds);

			clearInterval(countdownInterval);
			countdownInterval = setInterval(updateCountdown, 1000); // Start the countdown again
			return;
		}

		const daysValue = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
		const hoursValue = Math.floor((timeDifference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
		const minutesValue = Math.floor((timeDifference % (1000 * 60 * 60)) / (1000 * 60));
		const secondsValue = Math.floor((timeDifference % (1000 * 60)) / 1000);

		// Format the values using the formatTimeUnit function
		days = formatTimeUnit(daysValue);
		hours = formatTimeUnit(hoursValue);
		minutes = formatTimeUnit(minutesValue);
		seconds = formatTimeUnit(secondsValue);
	}

	function formatTimeUnit(unit: number): string {
		return unit.toString().padStart(2, '0');
	}

	onMount(() => {
		targetDate = new Date(Date.now() + twentyDaysInMilliseconds); // Set initial target date to 20 days from the current date
		updateCountdown(); // Initial call to update the countdown
		countdownInterval = setInterval(updateCountdown, 1000); // Update the countdown every second
	});

	onDestroy(() => {
		clearInterval(countdownInterval); // Clear the interval when the component is unmounted
	});
</script>

<section class="flex items-center gap-4">
	<div class="box-box">
		<div class="box">
			<p>{days}</p>
		</div>
		<p>days</p>
	</div>
	<div class="box-box">
		<div class="box">
			<p>{hours}</p>
		</div>
		<p>hrs</p>
	</div>
	<div class="box-box">
		<div class="box">
			<p>{minutes}</p>
		</div>
		<p>mins</p>
	</div>
	<div class="box-box">
		<div class="box">
			<p>{seconds}</p>
		</div>
		<p>secs</p>
	</div>
</section>

<style>
	.box-box {
		display: flex;
		align-items: center;
		flex-direction: column;
	}
	.box-box > p {
		margin-top: 0.35rem;
		font-size: 0.8rem;
	}
	.box {
		background-color: #fff;
		width: max-content;
		padding: 0.5rem;
		border-radius: 0.5rem;
	}
	.box p {
		font-family: 'Digital Numbers Regular';
	}
	p {
		text-transform: capitalize;
	}
</style>
