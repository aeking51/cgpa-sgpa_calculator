<script>
	import madewith from '$lib/images/made-with.png';
	import sbte from '$lib/images/sbte.jpeg';
	import sittr from '$lib/images/SITTR.png';
</script>
<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="text-column">
	<h1>About this Web App</h1>

	<p>
		&emsp;&emsp;It is hard to calculate CGPA and SGPA.But,
		CGPA and SGPA is essential for students to convert their grades into percentages, compare their performance across different semesters, and plan their study goals accordingly.
		But there will be always a difference in Calculating this values between different syllabuses.
		also, So we are created the CGPA / SGPA Calculator According to SITTR's Polytechnic diploma syllabus.In this web app we can easily Calculate CGPA and SGPA within minutes.
		<br>
		&emsp;&emsp;&emsp;CGPA and SGPA are grading systems used in colleges and universities to measure students academic performance.
		CGPA is the average of the grade points obtained by a student in all the semesters, while SGPA is the average of the grade points obtained by a student in a single semester.
		<br>
	</p>
	<br>
	<br><br>
	<div class="made">
		<img src= {madewith} alt="this app is made with" id="made-image" width="300">
	</div>
	<br><br><br>
	<div class="poi">
		<p>External Links</p>
		<a href="https://www.sbte.kerala.gov.in/" target="_blank"><img src={sbte} alt="sbte" width="150"></a>
		<a href="https://sitttrkerala.ac.in/" target="_blank"><img src={sittr} alt="sittr" width="130" height="40"></a>
	</div>
</div>

<style>
	.made{
		margin: 0 auto;
        margin-left: auto;
        margin-right: auto;
        text-align:center;
	}
	.poi{
		background-color: black;
		border-radius: 5px;
		color: whitesmoke;
		padding: 20px;
		margin-bottom: 0px;
	}

	@media screen and (max-width: 600px)
    {
		#made-image{
			width: 220px;
		}
	}
</style>
