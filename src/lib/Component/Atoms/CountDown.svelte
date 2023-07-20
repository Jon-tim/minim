<section class="flex items-center gap-4">
	<div class="box-box">
		<div class="box">
			<p>02</p>
		</div>
		<p>days</p>
	</div>
	<div class="box-box">
		<div class="box">
			<p>06</p>
		</div>
		<p>hrs</p>
	</div>
	<div class="box-box">
		<div class="box">
			<p>03</p>
		</div>
		<p>mins</p>
	</div>
	<div class="box-box">
		<div class="box">
			<p>20</p>
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
