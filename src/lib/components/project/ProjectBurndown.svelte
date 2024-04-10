<script>
	import { onMount } from 'svelte';

	onMount(async () => {
		const { default: ApexCharts } = await import('apexcharts');

		var options = {
			series: [
				{
					name: 'Expected',
					data: [10, 9, 8, 7, 6, 4, 2, 0]
				},
				{
					name: 'Actuals',
					data: [10, 9, 6, 5, 4, 2, 2, 0]
				}
			],
			chart: {
				height: 300,
				type: 'area',
				offsetX: -15,
				toolbar: {
					show: false
				}
			},
			dataLabels: {
				enabled: false
			},
			stroke: {
				curve: 'smooth'
			},
			xaxis: {
				type: 'datetime',
				categories: [
					'2023-06-20T00:00:00.000Z',
					'2023-07-20T01:30:00.000Z',
					'2023-08-20T02:30:00.000Z',
					'2023-09-20T03:30:00.000Z',
					'2023-10-20T04:30:00.000Z',
					'2023-11-20T05:30:00.000Z',
					'2023-12-20T06:30:00.000Z'
				]
			},
			tooltip: {
				x: {
					format: 'dd/MM/yy HH:mm'
				}
			}
		};

		var chart = new ApexCharts(document.querySelector('#chart'), options);

		chart.render();
	});
</script>

<div>
	<div id="chart"></div>
</div>
