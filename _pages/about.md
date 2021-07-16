---
title: "About"
permalink: "/about.html"
image: "assets/images/team.jpeg"
comments: false
---
<div class="container">
<div class="jumbotron jumbotron-fluid mb-3 pl-0 pt-0 pb-0 bg-white position-relative">
        <div class="h-100 tofront">
			<div class="row {% if page.image %} justify-content-between {% else %} justify-content-center {% endif %}">
				<div class="col-md-5 pr-0 align-self-center">
					<p>While the world is rapidly changing around us, Gen Z is forced to grapple with an uncertain future. So we decided to do something about it. We Need To Talk is a student-run, activism focused newspaper, that provides news for high-schoolers, by high-schoolers. We cover topics that are usually ignored by mainstream media, while providing the younger generation with a platform to make their voices heard.</p>
                    <p>
                    We offer a diverse set of perspectives on international issues, and bring student activism to the next level. Our writers are from all over the United States, Ethiopia, India, Pakistan, South Africa, and more.
                    </p>
				</div>
				<div class="col-md-7 pr-0 align-self-center">
					<img class="rounded" src="{% if page.image contains "://" %}{{ page.image }}{% else %}{{ site.baseurl }}/{{ page.image }}{% endif %}" alt="{{ page.title }}">
				</div>
			</div>
		</div>
	</div>
</div>




