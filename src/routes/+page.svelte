<script>
</script>

<svelte:head>
	<title>Kerala CGPA / SGPA Calculator</title>
	<meta name="description" content="CGPA Calculator" />
</svelte:head>

<section>
	<span class="welcome">
		<h1 class="heading"><span class="thin" style="color: black;">Kerala Polytechnic</span><br> CGPA <b>/</b> SGPA<br><span class="thin">Calculator</span></h1>
	</span>
	<br><br>
	<h2 class="select" style="margin-bottom: 0px;">
		Select an option to Calculate
	</h2>

	<div class="buttons">
		<a href="/cgpa"><button class="btn cgpa">CGPA</button></a>
		<a href="/sgpa"><button class="btn sgpa">SGPA</button></a>
	</div>

	<a href='https://i.postimg.cc/kXmPVMnD/method.jpg' border='0' alt='method' id='method' target="_blank">How We Calculate</a>

	<br><br>
	<p style="margin-bottom: 0;"><b>Vistor Counter</b></p>
	<img src="https://hitwebcounter.com/counter/counter.php?page=8536988&style=0024&nbdigits=6&type=page&initCount=0" alt="web counter"  border="0" /> 
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	.heading{
		width: 100%;
		color: var(--color-theme-1);
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
		font-weight: 900;
	}
	.thin{
		font-weight: 100;
		color: black;
	}
	.select{
		letter-spacing: 1.5pt;
		font-family: 'Source Sans Pro', sans-serif;
		font-size: 0.9rem;
		color:blue;
		text-shadow: 1px 1px orangered;
	}
	.buttons {
    margin: 10%;
    text-align: center;
	}

	.btn {
    width: 200px;
    font-size: 16px;
    font-weight: 600;
    color: #fff;
    cursor: pointer;
    margin: 20px;
    height: 55px;
    text-align:center;
    border: none;
    background-size: 300% 100%;

    border-radius: 50px;
    moz-transition: all .4s ease-in-out;
    -o-transition: all .4s ease-in-out;
    -webkit-transition: all .4s ease-in-out;
    transition: all .4s ease-in-out;
	}

	.btn:hover {
    background-position: 100% 0;
    moz-transition: all .4s ease-in-out;
    -o-transition: all .4s ease-in-out;
    -webkit-transition: all .4s ease-in-out;
    transition: all .4s ease-in-out;
	}

	.btn:focus {
    outline: none;
	}

	.btn.cgpa {
    background-image: linear-gradient(to right, #25aae1, #40e495, #30dd8a, #2bb673);
    box-shadow: 0 4px 15px 0 rgba(49, 196, 190, 0.75);
	}
	.btn.sgpa {
    background-image: linear-gradient(to right, #f5ce62, #e43603, #fa7199, #e85a19);
    box-shadow: 0 4px 15px 0 rgba(229, 66, 10, 0.75);
	}
	#method{
		color: rgb(59, 57, 57);
		font-weight: 600;
		text-shadow: 2px 2px #f5ce62;
		border: 0px solid black;
		padding: 15px;
		border-radius: 17px;
		box-shadow: 2px 2px 2px 2px rgba(0, 0, 0, 0.193);
	}
	#method:hover{
		text-shadow: 0px;
		font-weight: bold;
		text-decoration: none;
		text-shadow: none;
		border: 1px solid rgba(0, 0, 0, 0.193); 
		box-shadow: none;
		transition: 1s;
	}
	@media screen and (max-width: 600px)
    {
		#method{
			padding: 8px;
			font-size: 12px;
		}
		.select{
			margin-left: 8%;
		}
	}
</style>
