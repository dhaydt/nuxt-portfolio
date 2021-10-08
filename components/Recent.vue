<template>
  <!--recent-project---------------------------->
	<section id="recent">
	<!--heading--------------->
	<div class="recent-heading">
	<span>Recent</span>
	<h3>Recent Doing Project Design</h3>
	</div>
	<!--img--------------->
	<div class="recent-img">
		<img src="images/recent.png"/>
	</div>
	<!--btn----------->
	<a href="#" class="recent-btn">View Design</a>
	</section>

</template>

<script>
  export default {

  }
</script>

<style lang="scss" scoped>
#recent{
	display: flex;
	justify-content: center;
	align-items: center;
	margin:30px 0px;
	flex-direction: column;
}
.recent-heading span,
.client-heading span{
	color:#36b7b5;
	font-weight: 500;
	text-transform: uppercase;
	letter-spacing: 2px;
	font-size: 1.1rem;
}
.recent-heading h3,
.client-heading h3,
#contact h3{
	color:#1c3548;
	font-size: 3rem;
	margin: 0px;
	font-weight: 400;
	letter-spacing: 1px;
}
.recent-img{
	margin:0px 40px;
}
.recent-img img{
	width:100%;
	height: 100%;
}
.recent-btn{
	width:190px;
	height: 44px;
	display: flex;
	justify-content: center;
	align-items: center;
	color:#FFFFFF;
	background-color: #1db096;
	border-radius: 20px;
	box-shadow: 4px 10px 30px rgba(24,139,119,0.2);
}

.recent-btn:hover{
	background-color: #23cdaf;
	transition: all ease 0.2s;
}
.recent-btn{
	width:190px;
	margin-top: -20px;
}
</style>
