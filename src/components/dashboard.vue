<template>
	<div>
		<section>
			<div style="background-color:rgb(60, 183, 198);width:100%;height:200px;position:relative;">
				<nav style="background-color:rgb(60, 183, 198) !important;z-index:5" class="navbar navbar-expand-lg navbar-light">
					<router-link to="/user">
						<img v-bind:src="img" style="border-radius:50%;width:65px;height:65px;margin-top:10px;margin-left:0px;" alt="">
						<p style="margin-left:0px;font-weight:600; font-size:14px;color:black;">My profile</p>
					</router-link>
					<button @click="toggleNav()" style="margin-top:-20px;" class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbar" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
						<span style="color:white !important;font-size:30px;" class=" fa fa-bars"  data-toggle="collapse" data-target="#navbar" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation"></span>
					</button>
					<div v-if = "shownav" class="collapse navbar-collapse" id="navbar">
						<ul class="navbar-nav">
							<li class="nav-item active">
								<router-link to="/"><a class="nav-link" style="color:white" href="#">Home<span class="sr-only">(current)</span></a></router-link>
							</li>
							<li class="nav-item">
								<router-link to="/search"><a class="nav-link" style="color:white" href="#">Search</a></router-link>
							</li>
							<li class="nav-item">
								<router-link to="/portal"><a class="nav-link" style="color:white" href="#">Portal</a></router-link>
							</li>
						</ul>
					</div>
				</nav>

			</div>

			

			<div class="glide" style="margin-top:-70px;z-index:2">
				<div class="glide__track" data-glide-el="track" style="height:134px;">
					<ul class="glide__slides" style="height:134px;">
						<li class="glide__slide--active">
							<div style="width:100%;height:130px;box-shadow: 0 0.1em 0.2em 0 rgba(0,0,0,0.8);border-radius:5px;background:white;">
								<p style="padding:8px; overflow:auto;color:black;">
									{{user_name}} !<br>
									How are you<br>
									We are at your service.
									1
									<img src="~../assets/char1.png" style="width:60px;margin-top:15px;float:right;">	

								</p>
							</div>
						</li>
						<li class="glide__slide">
							<div style="width:100%;height:130px;box-shadow: 0 0.1em 0.2em 0 rgba(0,0,0,0.8);border-radius:5px;background:white;">
								<p style="padding:8px; overflow:auto;color:black;">
									{{user_name}} !<br>
									How are you<br>
									We are at your service.
									2
								</p>
								<img src="" alt="">	
							</div>
						</li>
						<li class="glide__slide">
							<div style="width:100%;height:130px;box-shadow: 0 0.1em 0.2em 0 rgba(0,0,0,0.8);border-radius:5px;background:white;">
								<p style="padding:8px; overflow:auto;color:black;">
									{{user_name}} !<br>
									How are you<br>
									We are at your service.
									3
								</p>
								<img src="" alt="">	
							</div>
						</li>
						<li class="glide__slide">
							<div style="width:100%;height:130px;box-shadow: 0 0.1em 0.2em 0 rgba(0,0,0,0.8);border-radius:5px;background:white;">
								<p style="padding:8px; overflow:auto;color:black;">
									{{user_name}} !<br>
									How are you<br>
									We are at your service.
									4
								</p>
								<img src="" alt="">	
							</div>
						</li>
					</ul>
				</div>
				<div class="glide__arrows" data-glide-el="controls">
					<i id="glideleft" class="glide__arrow glide__arrow--left fa fa-chevron-left" data-glide-dir="<"></i>
					<i id="glideright" class="glide__arrow glide__arrow--right fa fa-chevron-right" data-glide-dir=">"></i>
				</div>
			</div>
		</section>
		<section style="margin-top:40px;margin-bottom:20px; width:100%;height:100%;">
			<table style="width:100%;height:100%;">
				<tbody style="margin:0 auto;">
					<tr style="margin:0 auto;height:100px;">
						<td style="margin:0 auto;text-align:center;"><img src="~../assets/mybooking.png" style="height:100px;margin:0 auto;display:block" alt=""></td>
						<td style="margin:0 auto;text-align:center;"><router-link to="/payment"><img src="~../assets/payment.png" style="height:100px;margin:0 auto;display:block" alt=""></router-link></td>
						<td style="margin:0 auto;text-align:center;"><router-link to="/overheadBills"><img src="~../assets/overheadbills.png" style="height:100px;margin:0 auto;display:block" alt=""></router-link></td>
					</tr>
					<br>
					<tr style="margin:0 auto;height:100px;">
						<td v-on:click="downloadChecklist()" style="margin:0 auto;text-align:center;"><img src="~../assets/checklist.png" style="height:100px;margin:0 auto;display:block" alt=""></td>
						<td style="margin:0 auto;text-align:center;"><router-link to="/maintenanceUser"><img src="~../assets/maintenance.png" style="height:100px;margin:0 auto;display:block" alt=""></router-link></td>
						<td style="margin:0 auto;text-align:center;"><router-link to="/houseKeeping"><img src="~../assets/housekeeping.png" style="height:100px;margin:0 auto;display:block" alt=""></router-link></td>
					</tr style="margin:0 auto;">
					<br>
					<tr style="margin:0 auto;height:100px;">
						<td  v-on:click="downloadAgreement()" style="margin:0 auto;text-align:center;"><img src="~../assets/agreement.png" style="height:100px;margin:0 auto;display:block" alt=""></td>
						<td style="margin:0 auto;text-align:center;"><router-link to="/exitPage"><img src="~../assets/exithome.png" style="height:100px;margin:0 auto;display:block" alt=""></router-link></td>
						<td style="margin:0 auto;text-align:center;"><img src="~../assets/refer.png" style="height:100px;margin:0 auto;display:block" alt=""></td>
					</tr>
					
				</tbody>
			</table>
		</section>
	</div>
</template>

<script>
import firebase from 'firebase'
import store from '../vuex/store'
import Glide from '@glidejs/glide'
import { Controls } from '@glidejs/glide/dist/glide.modular.esm'
export default {
	data(){
		return{
			title: "my vue file",
			img:"https://img.favpng.com/21/13/5/user-profile-default-computer-icons-network-video-recorder-png-favpng-7dPZA8WRdY80Uw3bdMWkEN4fR.jpg",
			user_name:"",
			propertyId:"",
			uid:"",
			shownav : false
		}
	},
	methods:{
		toggleNav(){
			
			this.shownav = !this.shownav
		},
		downloadChecklist(){ // always we have to put pdf in database
			firebase.storage().ref("checklist/"+this.propertyId+".pdf").getDownloadURL().then(url =>{
				console.log(this.propertyId)
				window.open(url,'_blank')
			}).catch(err =>{
				console.log(err)
			})
		},
		downloadAgreement(){
			firebase.storage().ref("agreement/"+this.propertyId+".pdf").getDownloadURL().then(url =>{
				console.log(this.propertyId)
				window.open(url,'_blank')
			}).catch(err =>{
				console.log(err)
				
			})
		}
	},
	mounted(){
		this.$root.$children[0].$children[0].$el.style.display="none"; // to hide old nav bar  

		if(window.innerWidth > 480 )  // slider for desktop version
		{
			var glide = new Glide('.glide',{
			type: 'carousel',
			autoplay: 2000,
			bound:true,
			perView: 4,
			peek: 70,
			focusAt:0,
			animationTimingFunc: 'linear',
			animationDuration: 500,
			touchAngle:45,
			hoverpause:true,
			startAt:0,
			gap:30,
		})

		}
		else{									// slider for mobile version
			var glide = new Glide('.glide',{
			type: 'carousel',
			autoplay: 2000,
			bound:true,
			perView: 1,
			peek: 70,
			focusAt:0,
			animationTimingFunc: 'linear',
			animationDuration: 500,
			touchAngle:45,
			hoverpause:true,
			startAt:0,
			gap:30,
		})
		}
		

		glide.mount({Controls})



		
		if(user_profile!=false){  // if logged in via gmail
			firebase.firestore().collection('userProfile').doc(user_profile.getId()).get().then(res =>{
				if(res.data().personal.photo != undefined){
					this.img = res.data().personal.photo // get user image 
					this.user_name = res.data().personal.name				}

				}).catch(err =>{
					console.log(err)
				})
		}else{ // error on new registration
			var uid = store.state.email+store.state.phone;

			firebase.firestore().collection('userProfile').doc(uid).get().then(res =>{
				this.user_name = res.data().personal.name
			})

			firebase.storage().ref("userImage/"+uid).getDownloadURL().then(url =>{
				this.img = url;
			}).catch(err =>{
				this.img = "https://img.favpng.com/21/13/5/user-profile-default-computer-icons-network-video-recorder-png-favpng-7dPZA8WRdY80Uw3bdMWkEN4fR.jpg"
			})
		}
	
		if(window.innerWidth > 480){
			this.shownav =  true;
		}

		
		
	},
	created(){
		if(user_profile!=false){
			this.uid = user_profile.getId();
		}else{
			this.uid = store.state.email+store.state.phone;
		}

		firebase.firestore().collection('registeredUser').doc(this.uid).get().then(res =>{
			this.propertyId = res.data().propertyId
		})

	}

}
</script>

<style scoped>

@import url('../../node_modules/@glidejs/glide/dist/css/glide.theme.min.css');
@import url('../../node_modules/@glidejs/glide/dist/css/glide.core.min.css');
@import url('http://fonts.googleapis.com/css?family=Montserrat');
@import url("../../node_modules/bootstrap/dist/css/bootstrap.min.css");
@import url("../../node_modules/bootstrap/dist/css/bootstrap.css");

#glideright,#glideleft{
	border:0 !important;
	outline:0 !important;
	background:none !important;
	background-color:transparent !important;
	box-shadow:0px 0px 0px 0px;
	color:black !important;
	font-size:30px;
}
#glideright{
	margin-right:-50px;
	width:50px;
	height:50px;
}
#glideleft{
	margin-left:-50px;
	width:50px;
	height:50px;
}
.glide__arrow{
	box-shadow: 0 0em 0em 0 rgba(0,0,0,0.1) !important;
}
td img:active{
	transform:scale(0.97);
}


</style>
