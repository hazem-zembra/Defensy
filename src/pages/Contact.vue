<template>
	<div class="page-header clear-filter" filter-color="orange">
		<div class="page-header-image" style="background-image: url('img/contact.jpeg')"></div>
		<section class="ftco-section">
			<div class="container">
				<div class="row justify-content-center">
					<div class="col-lg-12 col-md-12">
						<div class="wrapper justify-content-center">
							<div class="row justify-content-center">
								<div class="col-lg-8 text-center mb-3 mt-5">
									<h2 class="typerclass">Contact Us</h2>
								</div>
								<div class="col-lg-4 text-center mb-3 mt-5">
								</div>
								<div class="col-lg-8 ">
									<div class="contact-wrap">
										<h3 class="mb-4 text-center">Please, fill in the form below and we'll get back ASAP.
										</h3>
										<div id="form-message-success" class="mb-4 w-100 text-center">
											Our Professional Services use open source security tools, customized by experts
											and leveraging the latest technology, to enhance clients' security posture and
											protect their systems and data.
										</div>
										<div id="contactForm" name="contactForm" class="contactForm">
											<div class="row">
												<div class="col-md-6">
													<div class="input-group">
														<input type="text" class="form-control" name="first_name" id="first_name" v-model="formData.first_name"
															placeholder="First Name" required>
													</div>
												</div>
												<div class="col-md-6">
													<div class="input-group">
														<input type="text" class="form-control" name="last_name" id="last_name" v-model="formData.last_name"
															placeholder="Last Name" required>
													</div>
												</div>
												<div class="col-md-6">
													<div class="input-group">
														<input type="text" class="form-control" name="business_name" id="business_name" v-model="formData.business_name"
															placeholder="Business Name" required>
													</div>
												</div>
												<div class="col-md-6">
													<div class="input-group">
														<input type="text" class="form-control" name="c_website" id="c_website" v-model="formData.c_website"
															placeholder="Company Website" required>
													</div>
												</div>
												
												<div class="col-md-6">
													<div class="input-group">
														<input type="email" class="form-control" name="email" id="email" v-model="formData.email"
															placeholder="E-mail" required>
													</div>
												</div>
												<div class="col-md-6">
													<div class="input-group">
														<input type="text" class="form-control" name="business_type" id="business_type" v-model="formData.business_type"
															placeholder="Business Type" required>
													</div>
												</div>
												<div class="col-md-6">
													<div class="input-group">
														<input type="text" class="form-control" name="package_detail" id="package_detail" v-model="formData.package_detail"
															placeholder="Package Details" required>
													</div>
												</div>
												<div class="col-md-6 ">
													<div class="input-group box-shadow">
														<input type="text" class="form-control form-control-no-box" name="project_budget" id="project_budget" v-model="formData.project_budget"
															placeholder="Project Budget" required>
															<span class="input-group-text border-radius-left">$</span>
													</div>
												</div>
												<div class="col-md-12">
													<div class="form-group">
														<textarea name="message" class="form-control border-radius" id="message" v-model="formData.message" cols="30"
															rows="8" placeholder="Message..." required></textarea>
													</div>
												</div>
												<div class="col-md-12">
													<div class="form-group">
														<input type="submit" @click="sendEmail" value="Send Message"
															class="btn btn-primary mx-auto">
														<div class="submitting"></div>
													</div>
												</div>
											</div>
										</div>
									</div>
								</div>
								<div class="col-lg-4 mb-5">
									<div class="row">
										<div class="col-md-12">
											<div class="dbox w-100 text-center">
												<div class="icon d-flex align-items-center justify-content-center">
													<span class="fa fa-map-marker-alt"></span>
												</div>
												<div class="text">
													<p><span style="color:white;font-weight: bold;">Address:</span>Pôle
														technologique Ghazela, Tunis</p>
												</div>
											</div>
										</div>
										<div class="col-md-12">
											<div class="dbox w-100 text-center">
												<div class="icon d-flex align-items-center justify-content-center">
													<span class="fa fa-phone"></span>
												</div>
												<div class="text">
													<p><span style="color:white;font-weight: bold;">Phone:</span> <a
															href="tel://1234567920">+216 54 33 00 20</a></p>
												</div>
											</div>
										</div>
										<div class="col-md-12">
											<div class="dbox w-100 text-center">
												<div class="icon d-flex align-items-center justify-content-center">
													<span class="fa fa-paper-plane"></span>
												</div>
												<div class="text">
													<p><span style="color:white;font-weight: bold;">Email:</span> <a
															href="mailto:info@yoursite.com">contact@raiseguard.net</a></p>
												</div>
											</div>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</section>
	</div>
</template>
<script>
import { Button, FormGroupInput } from '@/components';
import axios from 'axios';
export default {
	data(){
		return {
			formData : {
				first_name : '',
				last_name : '',
				business_name : '',
				c_website : '',
				email : '',
				business_type : '',
				package_detail : '',
				project_budget : '',
				message : '',
				errorMessage : '',
				successMessage : ''
			}
		};
	},
	methods :{
		sendEmail() {
			console.log('Hi');
    const apiKey = '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';
    const apiUrl = 'https://api.sendinblue.com/v3/smtp/email';
	let name = this.formData.first_name + ' ' + this.formData.last_name; 
	let message_to_send = '<h3>'+this.formData.first_name + this.formData.last_name +'</h3><h4>Business name: '+ this.formData.business_name +'</h4><h4>Business type: '+ this.formData.business_type +'</h4><h4>Package detail: '+ this.formData.package_detail + '</h4><h4>Project budget: '+this.formData.project_budget+'$</h4><p><strong>Other informations: </strong>'+ this.formData.message +' </p><ul><li><strong>Email: </strong>'+ this.formData.email + '</li><li><strong>Website :</strong>'+ this.formData.c_website +'</li></ul>';
    const payload = {
      sender: {
        //name: first_name + last_name,
        name:name,
		email: 'ha.zem.abbassi6@gmail.com',
      },
      to: [
        {
          email: 'ha.zem.abbassi6@gmail.com',
          name: 'RAISEGUARD',
        },
      ],
      subject: 'Contact',
      //htmlContent: '<h3>'+first_name + last_name +'</h3><h4>Business name: '+business_name + business_type + '</h4><h4>'+ package_detail + '</h4><h4>'+ project_budget + '</h4><p> '+ message +' </p><ul><li>'+ email + '</li><li>'+ c_website +'</li></ul>',
	htmlContent: message_to_send,
	};
console.log('Test');
    axios
      .post(apiUrl, payload, {
        headers: {
          'api-key': apiKey,
          'Content-Type': 'application/json',
        },
      })
      .then(response => {
        console.log('Email sent successfully:', response.data);
      })
      .catch(error => {
        console.error('Failed to send email:', error);
      });
  },		

	},
	name: 'login-page',
	bodyClass: 'login-page',
	components: {
		[Button.name]: Button,
		[FormGroupInput.name]: FormGroupInput
	}
};
</script>
<style>
.ftco-section {
	padding: 7em 0;
}

.dbox {
	width: 100%;
	margin-bottom: 25px;
	padding: 0 20px;
}

@media (min-width: 768px) {
	.dbox {
		margin-bottom: 0;
		padding: 0;
	}
}

.dbox p {
	margin-bottom: 0;
}

.dbox p span {
	font-weight: 500;
	color: #03224c;
	display: block;
}

.dbox p a {
	color: rgba(255, 255, 255, 0.8);
}

.dbox .icon {
	width: 60px;
	height: 60px;
	border-radius: 50%;
	background: #03224c;
	margin: 0 auto;
	margin-bottom: 20px;
}

.dbox .icon span {
	font-size: 20px;
	color: #fff;
}

.dbox .text {
	width: 100%;
}

.w-100 {
	width: 100% !important;
}

.d-flex {
	display: -webkit-box !important;
	display: -ms-flexbox !important;
	display: flex !important;
}

.contact-wrap h3 {
	color: #fff;
}

.contactForm .label {
	color: #fff;
	text-transform: uppercase;
	font-size: 12px;
	font-weight: 600;
}

.contactForm .form-control {
	border: none;
}

.contactForm .btn {
	width: 100%;
	display: block;
}

</style>
