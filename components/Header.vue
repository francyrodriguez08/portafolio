<template>
    <div class="wrapper_header">
      <div class="container_img">
				<div class="wrapper_img">
        	<img src="../assets/perfil.jpg" alt="">
				</div>
      </div>
      <div class="container_name">
        <span class="name">Francy</span>
        <span class="lastname">Rodriguez</span>
        <span class="profession">Designer UI/UX</span>
      </div> 
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
	.wrapper_header{
		/* max-width: 900px; */
		/* width: 100%; */
		display: flex;
		/* background-color: #efefef; */
	}
	.container_img{
		/* border: 1px solid red; */
	}
	.wrapper_img{
		width: 220px;
		height: 220px;
		border-radius: 50%;
		position: relative;
		z-index: 4;
	}
	.wrapper_img::before{
		content: '';
		position: absolute;
		width: 240px;
		height: 240px;
		background-color: var(--primary);
		border-radius: 50%;
		z-index: -1;
	}
	.wrapper_img::after{
		content: '';
		position: absolute;
		width: 240px;
		height: 240px;
		border: 4px solid #000;
		border-radius: 50%;
		z-index: -1;
		position: absolute;
		top: -10px;
		left: -10px;
	}
	img{
		width: 100%;
		height: 100%;
		object-fit: cover;
		border-radius: 50%;
	}
	.container_name {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding-left: 80px;
		justify-content: center;
	}
	.container_name span{
		line-height: 1;
	}
	.name{
		font-size: 4rem;
		text-transform: uppercase;
		font-weight: 400;
		position: relative;
	}
	.name::after{
		content: '';
		position: absolute;
		width: 70px;
		height: 15px;
		background: var(--primary);
		border-radius: 1rem;
		top: 0;
		margin-left: 20px ;
	}
	.lastname{
		font-size: 4rem;
		text-transform: uppercase;
		font-weight: bold;
		padding-left: 2.5rem;
	}
	.profession{
		font-size: 1.5rem;
		padding-left: 9rem;
		letter-spacing: 1px;
		position: relative;
	}
	.profession::before{
		content: '';
		position: absolute;
		width: 100px;
		height: 15px;
		background: var(--primary);
		border-radius: 1rem;
		top: 7px;
		right: -110px;
	}
	.profession::after{
		content: '';
		position: absolute;
		width: 50px;
		height: 15px;
		background: var(--primary);
		border-radius: 1rem;
		top: 7px;
		margin-left: 20px ;
	}
	@media (max-width: 600px){
		.wrapper_header{
			display: flex;
			flex-direction: column;
			align-items: center;
			margin-top: -70px;
		}
		.wrapper_img{
			width: 180px;
			height: 180px;
		}
		.wrapper_img::before{
			width: 200px;
			height: 200px;
		}
		.wrapper_img::after{
			width: 200px;
			height: 200px;
		}
		.name{
			font-size: 2.2rem;
		}
		.name::after{
			display: none;
		}
		.lastname{
			font-size: 2.2rem;
			text-transform: uppercase;
			font-weight: bold;
			padding-left: 0;
		}
		.profession{
			font-size: 1.2rem;
			padding-left: 0;
			letter-spacing: 1px;
			position: relative;
		}
		.profession::before{
			top: 30px;
			left: 0;
			margin-left: 30px;
		}
		.profession::after{
			display: none;
		}
		.container_name {
			margin-top: 40px;
			padding-left: 0;
			align-items: center;
		}
	}
</style>